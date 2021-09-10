# Projeto 1 - Ciência dos Dados
Classificador de Tweets

# Método de classificação de relevância: 
O tweet para ser considerado RELEVANTE (1) deve estar atrelado ao filme "Spiderman: No Way Home", abordando tanto especulações sobre personagens do filme quanto a ansiedade para vê-lo. Lembrando que tweets que, por exemplo, falem sobre o MCU (Marvel Cinematographic Universe), como Homem de Ferro, Vingadores e Eternos, com ou sem o Spiderman, são considerados IREELEVANTES (0).

# CLASSIFICADOR DE RELEVÂNCIA
- MUITO IRRELEVANTE = 0
- IRRELEVANTE = 1
- NEUTRO = 2
- RELEVANTE = 3
- MUITO RELEVANTE = 4


MUITO IRRELEVANTE: falando de outro assunto, não envolve o iPhone, pessoas que não sabem tweetar ou se comunicar (Ex: só colocou uma hashtag)
IRRELEVANTE: anúncios de venda (EX: venha comprar no magalu)
NEUTRO: piada sobre o iPhone (EX: iPhone é o Corsa em miniatura kkkkkk)
RELEVANTE: comentário indireto relacionado ao iPhone (EX: meu professor de ciências passou 30 minutos só falando do novo iPhone dele)
MUITO RELEVANTE: falando objetivamente do iPhone, tipo opinião, dúvida ou desejo de comprar (EX: iPhone 13 vai esperar um pouco para chegar em minhas mãos)