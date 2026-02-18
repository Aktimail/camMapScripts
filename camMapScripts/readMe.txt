des ptits scripts pour aller un peu plus vite en camera mapping sur maya ^^

-attributeNameScript-
renvoie touts les nom d'attributs de l'objet selectionné (long name et short name)

-colorSpaceManagerScript-
selectionne les nodes files des materiaux auquels tu veux appliquer un nouveau colorspace

-defautCamMapMaterialScript-
attention a bien avoir créé une camera nommée "camProj" et sa shape "camProjShape"
flags:
cameraRef : str / le nom de la SHAPE de la caméra lié / par défaut : "camProjShape"
colorSpace : str / nom du colorspace / par défaut : "Raw"
ignoreCsFileRules : bool / si =True ignore les regles lié au colorspace / par défaut : False

les flags sont à rajouter entre les parenthaises de la dernière ligne du script appelant la fonction assignDefaultMat
exemple :
assignDefaultMat(cameraRef="linkedCameraShape")
assignDefaultMat(colorSpace="sRGB")
assignDefaultMat(ignoreCsFileRules=True)
assignDefaultMat(cameraRef="linkedCameraShape", ignoreCsFileRules=True)

-initFilePathScript-
selectionne les nodes files des materiaux
corrige les chemins de fichiers
attention à laisser un "/" à la fin
"../" reviens en arriere dans le chemin



écrit le 18/02/2026 par Antoine Bouchareine