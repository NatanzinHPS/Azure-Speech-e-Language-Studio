# Azure Speech Studio e Language Studio - Laboratório Prático

## 📋 Sobre o Projeto

Este repositório documenta minha experiência prática com as ferramentas **Azure Speech Studio** e **Language Studio**, explorando recursos de inteligência artificial para análise de fala e processamento de linguagem natural. O objetivo é demonstrar a aplicação dos conceitos aprendidos e criar um material de referência para futuras implementações.

## 🎯 Objetivos de Aprendizagem

- ✅ Aplicar conceitos de IA em ambiente prático
- ✅ Documentar processos técnicos de forma estruturada
- ✅ Utilizar GitHub para compartilhamento de documentação técnica
- ✅ Explorar funcionalidades do Azure Speech Studio
- ✅ Implementar soluções com Language Studio

## 🛠️ Ferramentas Utilizadas

### Azure Speech Studio
- **Conversão de Fala em Texto (Speech-to-Text)**
- **Conversão de Texto em Fala (Text-to-Speech)**
- **Tradução de Fala**
- **Identificação do Locutor**

### Azure Language Studio
- **Análise de Sentimento**
- **Extração de Entidades**
- **Classificação de Texto**
- **Detecção de Idioma**

## 📊 Experiências Práticas

### 1. Azure Speech Studio

#### 🎤 Speech-to-Text (Conversão de Fala em Texto)

**Objetivo**: Converter áudio em texto com alta precisão

**Processo Realizado**:
1. Acesso ao Azure Speech Studio
2. Seleção do serviço Speech-to-Text
3. Upload de arquivo de áudio / Gravação ao vivo
4. Configuração de idioma e modelo
5. Processamento e análise dos resultados

**Insights Adquiridos**:
- A precisão varia significativamente com a qualidade do áudio
- Ruídos de fundo impactam negativamente na transcrição
- Diferentes sotaques podem afetar a acurácia
- Suporte robusto para múltiplos idiomas, incluindo português brasileiro

**Exemplo de Teste Realizado**:
```
Áudio Original: "Olá, meu nome é Natan e estou testando o Azure Speech Studio"
Resultado: "Olá, meu nome é Natan e estou testando o Azure Speech Studio"
Precisão: 100% (áudio limpo, sem ruído)

Áudio com Ruído: "Bom dia, como vocês estão hoje?" (com música de fundo)
Resultado: "Bom dia, como vocês estão oje?"
Precisão: ~85% (falha na palavra "hoje")
```

**Casos de Uso Identificados**:
- Transcrição de reuniões e conferências
- Legendas automáticas para vídeos
- Assistentes virtuais
- Acessibilidade para pessoas com deficiência auditiva

#### 🔊 Text-to-Speech (Conversão de Texto em Fala)

**Objetivo**: Gerar fala natural a partir de texto

**Processo Realizado**:
1. Inserção de texto para conversão
2. Seleção de voz (masculina/feminina)
3. Ajuste de velocidade e tom
4. Configuração de idioma e sotaque
5. Geração e download do áudio

**Insights Adquiridos**:
- Qualidade de voz surpreendentemente natural
- Ampla variedade de vozes disponíveis
- Controle fino sobre prosódia e entonação
- Suporte para SSML (Speech Synthesis Markup Language)

**Exemplo de Teste Realizado**:
```
Texto Input: "Bem-vindos ao laboratório de Azure AI! Hoje vamos explorar as funcionalidades incríveis do Speech Studio."
Configuração: Voz feminina brasileira, velocidade normal
Resultado: Áudio com pronúncia natural e entonação adequada

Teste com SSML:
<speak>
    <voice name="pt-BR-FranciscaNeural">
        Olá! <break time="500ms"/> Como vocês estão?
        <prosody rate="slow">Vamos falar mais devagar agora.</prosody>
    </voice>
</speak>
```

**Aplicações Práticas**:
- Audiobooks e conteúdo educacional
- Sistemas de navegação
- Chatbots com resposta por voz
- Acessibilidade para pessoas com deficiência visual

### 2. Azure Language Studio

#### 💭 Análise de Sentimento

**Objetivo**: Identificar o tom emocional de textos

**Processo Realizado**:
1. Inserção de textos em português
2. Execução da análise de sentimento
3. Interpretação dos scores de confiança
4. Teste com diferentes tipos de conteúdo

**Resultados Observados**:
- Classificação precisa entre positivo, negativo e neutro
- Scores de confiança auxiliam na interpretação
- Boa performance com gírias e expressões brasileiras
- Detecção de sentimentos mistos em textos complexos

**Exemplos de Testes Realizados**:
```
Texto 1: "Adorei o atendimento! A equipe foi super atenciosa e o produto é excelente."
Resultado: Positivo (Score: 0.98)

Texto 2: "O serviço foi péssimo, demorou muito e ainda veio com defeito."
Resultado: Negativo (Score: 0.95)

Texto 3: "O produto é ok, nada demais mas serve para o básico."
Resultado: Neutro (Score: 0.76)

Texto 4: "Que massa! Ficou irado esse projeto, véi!"
Resultado: Positivo (Score: 0.89) - Reconheceu gírias brasileiras
```

**Casos de Uso**:
- Monitoramento de redes sociais
- Análise de feedback de clientes
- Avaliação de reviews de produtos
- Pesquisas de opinião automatizadas

#### 🏷️ Extração de Entidades

**Objetivo**: Identificar e classificar entidades em textos

**Processo Realizado**:
1. Análise de textos diversos (notícias, emails, documentos)
2. Identificação automática de entidades
3. Classificação por categorias (pessoa, local, organização, etc.)
4. Avaliação da precisão das extrações

**Entidades Detectadas**:
- **Pessoas**: Nomes próprios e referências pessoais
- **Locais**: Cidades, países, endereços
- **Organizações**: Empresas, instituições
- **Datas**: Diferentes formatos temporais
- **Valores**: Números, moedas, porcentagens

**Exemplo de Teste Realizado**:
```
Texto Input: "Natan trabalha na Microsoft em São Paulo desde janeiro de 2024, 
ganhando R$ 15.000 por mês. Ele se formou na USP em 2022."

Entidades Extraídas:
- Pessoa: "Natan" (Confiança: 0.99)
- Organização: "Microsoft" (Confiança: 0.97)
- Local: "São Paulo" (Confiança: 0.98)
- Data: "janeiro de 2024" (Confiança: 0.95)
- Valor: "R$ 15.000" (Confiança: 0.92)
- Organização: "USP" (Confiança: 0.89)
- Data: "2022" (Confiança: 0.91)
```

**Aplicações Identificadas**:
- Processamento automático de documentos
- Análise de contratos e textos legais
- Indexação inteligente de conteúdo
- Sistemas de busca avançada

## 🔍 Análises e Descobertas

### Pontos Fortes das Ferramentas

1. **Interface Intuitiva**: Ambas as plataformas oferecem interfaces user-friendly
2. **Precisão Elevada**: Resultados consistentes e confiáveis
3. **Suporte ao Português**: Excelente compatibilidade com português brasileiro
4. **Escalabilidade**: Capacidade de processar grandes volumes de dados
5. **Integração**: APIs bem documentadas para integração em aplicações

### Desafios Encontrados

1. **Qualidade do Áudio**: Speech-to-Text sensível a ruídos
2. **Contexto Cultural**: Algumas expressões específicas podem ser mal interpretadas
3. **Custos**: Necessário considerar pricing para uso em produção
4. **Latência**: Tempo de processamento pode variar conforme complexidade

## 🚨 Erros Encontrados e Soluções

### Erro 1: "InvalidApiKeyError" no Speech Studio
**Problema**: Erro de autenticação ao tentar acessar o serviço
```
Status: 401 Unauthorized
Erro: "Access denied due to invalid subscription key"
```
**Causa**: Chave de API incorreta ou expirada
**Solução**: 
1. Verificar se a chave foi copiada corretamente (sem espaços extras)
2. Confirmar se o recurso está na região correta
3. Regenerar a chave no Azure Portal se necessário

### Erro 2: Transcrição Incorreta com Sotaque Regional
**Problema**: Speech-to-Text não reconheceu corretamente palavras com sotaque nordestino
```
Fala: "Oxente, que massa esse sistema!"
Resultado: "Oxente, que massa esse sistema!" ✅
Fala: "Véi, tá de boa esse negócio"
Resultado: "Veio, tá de boa esse negócio" ❌
```
**Solução**:
1. Usar modelo customizado treinado com dados regionais
2. Pós-processar resultados com dicionário de correções
3. Ajustar configurações de confiança

### Erro 3: Text-to-Speech com Pronúncia Incorreta
**Problema**: Palavras estrangeiras pronunciadas de forma inadequada
```
Texto: "Vamos fazer um workshop sobre machine learning"
Problema: "workshop" pronunciado como "vórkshop"
```
**Solução**:
1. Usar notação fonética no SSML
```xml
<speak>
Vamos fazer um <phoneme alphabet="ipa" ph="ˈwɜrkʃɒp">workshop</phoneme>
sobre machine learning
</speak>
```
2. Substituir por equivalentes em português quando apropriado

### Erro 4: Language Studio - Falso Positivo em Análise de Sentimento
**Problema**: Ironia não detectada corretamente
```
Texto: "Que maravilha, mais um dia de chuva no fim de semana!"
Resultado: Positivo (Score: 0.72) ❌
Esperado: Negativo (ironia)
```
**Solução**:
1. Combinar com análise de contexto
2. Implementar regras de pós-processamento
3. Usar modelos fine-tuned para detecção de ironia

## 📚 Recursos e Referências

### Documentação Oficial
- [Azure Speech Studio Documentation](https://docs.microsoft.com/azure/cognitive-services/speech-service/)
- [Azure Language Studio Documentation](https://docs.microsoft.com/azure/cognitive-services/language-service/)
- [Azure AI Services](https://azure.microsoft.com/services/cognitive-services/)

### Tutoriais e Guias
- [Speech-to-Text Quickstart](https://docs.microsoft.com/azure/cognitive-services/speech-service/get-started-speech-to-text)
- [Text Analytics API](https://docs.microsoft.com/azure/cognitive-services/text-analytics/)
- [Best Practices Guide](https://docs.microsoft.com/azure/cognitive-services/speech-service/how-to-custom-speech)

---

## ✨ Conclusão

A experiência com Azure Speech Studio e Language Studio demonstrou o potencial transformador da inteligência artificial aplicada ao processamento de voz e linguagem natural. As ferramentas oferecem capacidades robustas que podem ser aplicadas em diversos cenários, desde soluções de acessibilidade até sistemas complexos de análise de sentimento.

O aprendizado adquirido neste laboratório fornece uma base sólida para implementações futuras e serve como referência para projetos que envolvam processamento inteligente de conteúdo em português brasileiro.

**Desenvolvido por**: Natan  
**Data**: 25 de Maio de 2025  
**Desafio**: DIO - Azure AI Fundamentals
