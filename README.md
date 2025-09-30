# Funcionalidades Implementadas - Mapa Interativo de Ocorrências

## ✅ Funcionalidades Principais

### 1. **Upload de Excel Dinâmico**

- Upload de arquivos Excel (.xlsx, .xls) via clique ou arrastar e soltar
- Detecção automática de colunas (Municípios, Estado, Nº Ocorrências)
- Processamento inteligente de nomes de municípios (remove estado do nome)
- Matching automático com dados do GeoJSON
- Feedback visual do processo de upload

### 2. **Controles de Visualização no Header**

- **📁 Ocultar/Exibir Upload**: Controla a visibilidade da seção de upload
- **📊 Ocultar/Exibir Stats**: Controla a visibilidade das estatísticas
- **🔍 Maximizar/Restaurar Mapa**: Maximiza o mapa ocultando todas as outras seções

### 3. **Estatísticas Dinâmicas**

- **Total de Ocorrências**: Soma de todas as ocorrências
- **Municípios com Ocorrências**: Contagem de municípios que têm ocorrências > 0
- **Estados Afetados**: Número de estados que têm municípios com ocorrências
- **Média por Município**: Média de ocorrências por município afetado

### 4. **Funcionalidades do Mapa**

- Visualização de municípios coloridos por número de ocorrências
- Tooltips com nome do município e número de ocorrências
- Popups com informações detalhadas ao clicar
- Zoom automático para municípios selecionados
- Labels aparecem automaticamente em zoom >= 9

### 5. **Tabela Interativa**

- Lista todos os municípios com ocorrências ordenados por quantidade
- Clique na linha da tabela para navegar para o município no mapa
- Atualização automática quando dados são carregados

### 6. **Gestão de Dados**

- Botão "Resetar para Dados Originais" para voltar aos dados iniciais
- Backup automático dos dados originais
- Aplicação dinâmica dos dados do Excel sem modificar arquivos originais

## 🎯 Formato do Excel Esperado

O arquivo Excel deve ter as seguintes colunas (nomes detectados automaticamente):

- **MUNICIPIOS** ou variações (Município, Cidade, NM_MUN)
- **ESTADO** ou variações (UF, Sigla)
- **Nº OCORRÊNCIAS** ou variações (Ocorrências, Número, Qtd, Quantidade)

### Exemplo de formato aceito:

```
MUNICIPIOS               ESTADO    Nº OCORRÊNCIAS
ACOPIARA - CE           CE        2
AFOGADOS DA INGAZEIRA   PE        3
AGRESTINA               PE        2
```

## 🚀 Como Usar

1. **Carregamento Inicial**: O mapa carrega com dados zerados de 10 estados (PE, PB, AL, BA, CE, RN, MA, PA, PI, TO)
2. **Upload de Dados**: Clique na área de upload ou arraste um arquivo Excel
3. **Visualização**: Os dados são aplicados automaticamente ao mapa
4. **Controles**: Use os botões no header para otimizar a visualização
5. **Reset**: Use o botão de reset para voltar aos dados originais

## 🗺️ Estados Suportados

O sistema agora suporta 10 estados com seus respectivos municípios:

- **PE** - Pernambuco
- **PB** - Paraíba
- **AL** - Alagoas
- **BA** - Bahia
- **CE** - Ceará
- **RN** - Rio Grande do Norte
- **MA** - Maranhão
- **PA** - Pará
- **PI** - Piauí
- **TO** - Tocantins

## 🎨 Melhorias de UX

- **Responsivo**: Interface se adapta a diferentes tamanhos de tela
- **Feedback Visual**: Cores e animações indicam ações e estados
- **Controles Intuitivos**: Botões com ícones e textos descritivos
- **Maximização**: Opção de maximizar o mapa para análise detalhada
- **Estatísticas**: Cards coloridos com informações importantes
