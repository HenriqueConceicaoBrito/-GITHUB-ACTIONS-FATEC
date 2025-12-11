name: Pipeline Simples

on:
  push:
    branches: [main, develop]
  pull_request:
    branches: [main]

jobs:
  build:
    name: Construir e Testar
    runs-on: ubuntu-latest
    
    steps:
      # 1. Baixar o código
      - name: Checkout do código
        uses: actions/checkout@v4
      
      # 2. Configurar ambiente
      - name: Configurar ambiente
        run: |
          echo "🔧 Configurando ambiente..."
          echo "Versão do Node: $(node --version)" || echo "Node não instalado"
          echo "Versão do Python: $(python --version)" || echo "Python não instalado"
          echo "Sistema: $(uname -a)"
      
      # 3. Verificar estrutura do projeto
      - name: Verificar arquivos
        run: |
          echo "📁 Estrutura do projeto:"
          ls -la
          echo ""
          echo "📄 Arquivos importantes:"
          [ -f "package.json" ] && echo "✓ package.json encontrado" || echo "✗ package.json não encontrado"
          [ -f "requirements.txt" ] && echo "✓ requirements.txt encontrado" || echo "✗ requirements.txt não encontrado"
          [ -f "README.md" ] && echo "✓ README.md encontrado" || echo "✗ README.md não encontrado"
      
      # 4. Simular build
      - name: Simular Build
        run: |
          echo "🚀 Iniciando build..."
          echo "📦 Instalando dependências..."
          echo "🔨 Compilando projeto..."
          echo "✅ Build concluído com sucesso!"
      
      # 5. Simular testes
      - name: Executar Testes
        run: |
          echo "🧪 Executando testes..."
          echo "✓ Teste 1: Passou"
          echo "✓ Teste 2: Passou"
          echo "✓ Teste 3: Passou"
          echo "🎯 3/3 testes passaram"
      
      # 6. Finalizar
      - name: Relatório Final
        run: |
          echo "========================================"
          echo "🏁 PIPELINE CONCLUÍDA COM SUCESSO!"
          echo "========================================"
          echo "📊 Status: ✅ APROVADO"
          echo "👤 Executor: ${{ github.actor }}"
          echo "📅 Data: $(date)"
          echo "🔗 Commit: ${{ github.sha }}"
          echo "🌐 Branch: ${{ github.ref }}"
          echo "========================================"
