# Aplicacoes-de-operacoes-aritmeticas-em-imagens

import cv2

# leitura e carregamento da imagem a ser subtraída, a que não contém a caneta

img_1 = cv2.imread('sem_caneta.jpg')

![sem_caneta](https://github.com/Nicolas-HGS/Aplicacoes-de-operacoes-aritmeticas-em-imagens/assets/141871267/e3733600-3739-4194-8c07-8df1b6d6a4b8)

# leitura e carregamento da imagem que fará a subtração, a que contém a caneta

img_2 = cv2.imread('com_caneta.jpg')

![com_caneta](https://github.com/Nicolas-HGS/Aplicacoes-de-operacoes-aritmeticas-em-imagens/assets/141871267/34c19a35-9070-430b-bcc5-0fe52c2d5c2a)

# imagem resultante da subtração, exibirá a diferença entre as duas imagens, cujo objetivo é destacar a caneta

img_3 = cv2.subtract(img_1,img_2)

![diferenca](https://github.com/Nicolas-HGS/Aplicacoes-de-operacoes-aritmeticas-em-imagens/assets/141871267/02cc8a87-b0aa-414e-a21e-45ab8cee3dc7)

# ajustando a janela de exibição

cv2.namedWindow("Resize", cv2.WINDOW_NORMAL)
cv2.resizeWindow("Resize", 300, 300)

# concatenando as imagens para serem exibidas lado a lado

img_f = cv2.hconcat([img_1,img_2,img_3])

#exibição das imagens lado a lado

cv2.imshow('Resize',img_f)

![diferenca](https://github.com/Nicolas-HGS/Aplicacoes-de-operacoes-aritmeticas-em-imagens/assets/141871267/cc53a010-48f2-49e1-846f-d4c6b068e172)

# mantém a janela de exibição até alguma tecla ser pressionada

cv2.waitKey(0)
