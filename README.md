# Detecção Glaucoma

Fluxo de trabalho experimento 1

![experiment001 (1)](https://github.com/Noirane/glaucoma/assets/79718537/51b1f0d4-cbb3-4428-90fb-f5b91f0976ff)

Exemplos de previsões experimento 1


![previsoesEx1](https://github.com/Noirane/glaucoma/assets/79718537/e1055008-ff93-47b0-9ec9-327315c08450)


Fluxo de trabalho experimento 2 


![experiment002](https://github.com/Noirane/glaucoma/assets/79718537/2eceeb65-58a5-4575-8a71-7cb0b7efb366)


Exemplos de previsões experimento 2
![previsoes002](https://github.com/Noirane/glaucoma/assets/79718537/3801b96d-b228-4a7a-a7d8-9aab7ffb64ff)




Projeto desenvolvido no mestrado em Ciência da computação, na disciplina de visão computacional. 

O AIROGS Dataset consiste em uma coleção de imagens coloridas do fundo do olho de 60.357 indivíduos, totalizando 113.893 imagens, com várias dimensões. O conjunto de dados inclui indivíduos de aproximadamente 500 locais diferentes, representando uma população étnica diversificada. Uma tabela é fornecida, contendo duas colunas: challenge\_id, que inclui os nomes das imagens, e class, que indica a classificação como: glaucoma remissível (RG) ou glaucoma não remissível (NRG)

Como os rótulos de treinamento não continham informações sobre a localização do disco óptico, foi necessário realizar a segmentação manual. No experimento 1, 4.177 imagens foram redimensionadas para 512x512 pixels. Em seguida, 500 dessas imagens passaram por marcação manual do disco óptico por meio do aplicativo LabelImg. Cada imagem rotulada tinha uma anotação XML indicando a localização do disco óptico. As 500 imagens, junto com suas anotações XML, foram usadas como entrada para o Detectron 2 gerar 4.177 discos ópticos recortados com dimensões de 390x390 pixels. 

Para os experimentos 2 e 3, o conjunto de dados de imagem manteve suas dimensões originais. Um total de 1.000 imagens foram rotuladas manualmente usando o aplicativo LabelImg para esses dois experimentos.

Todos experimentos utilizaram o modelo : FASTERRCNN_RESNET50_FPN para detecção do glaucoma. 

No experimento 1, foram utilizadas 4.177 imagens do disco óptico, divididas da seguinte forma: o conjunto de teste foi definido como 10% do tamanho total do conjunto de treinamento (417 imagens), enquanto o conjunto de validação correspondeu a 20% do tamanho total do treinamento tamanho definido (835 imagens), com as imagens restantes (2925) alocadas para treinamento.

Nos experimentos 2 e 3, foram utilizadas 1.000 imagens do fundo de olho com discos ópticos marcados manualmente. O tamanho do conjunto de teste foi definido como 10% do tamanho total (100 imagens), enquanto o tamanho do conjunto de validação correspondeu a 20% do tamanho total (200 imagens), com as imagens restantes (700) alocadas para treinamento.


Link do dataset e modelos: [Link do dataset](https://drive.google.com/drive/folders/1B_1S1wijMYmG6nOoYVT9eSL46qUloaiC?usp=sharing/)

Link do desafio: [AiroGS Grand Challenge](https://airogs.grand-challenge.org/)

