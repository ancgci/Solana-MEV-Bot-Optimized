
<h2 align="center"><a href="https://github.com/ancgci" target="_blank">Oi 👋, eu gosto muito de assuntos referente a Blockchain, você pode me contatar 👈🏻</a></h2>

# Solana MEV Bot

Bem-vindo ao **Solana MEV Bot**! Este bot baseado em Rust foi projetado para executar estratégias de Maximal Extractable Value (MEV) na blockchain Solana.

🚀 **Este projeto é um fork do repositório original pertencente a** [BitFancy](https://github.com/BitFancy).  

Certifique-se de ter os seguintes itens instalados:

- **Rust**: Instale o Rust usando rustup:
  ```bash
  curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
  ```

- **Solana CLI**: Instale executando:
   ```bash
  sh -c "$(curl -sSfL https://release.solana.com/stable/install)"
  ```

### Instalação

1. Clone o repositório:
 ```bash
   git clone https://github.com/BitFancy/Solana-MEV-Bot-Optimized.git
   cd Solana-MEV-Bot-Optimized
   ```

3. Compile o projeto:
  ```bash
   cargo build --release
   ```

5. Configure seu ambiente:
   - Crie um arquivo `.env` no diretório raiz e adicione sua chave privada da carteira Solana e o link RPC:
      ```
     SOLANA_WALLET_PRIVATE_KEY=YOUR_PRIVATE_KEY
     DEFAULT_RPC=https://api.mainnet-beta.solana.com
     ```

## Executando o Projeto

Para executar o bot, use o seguinte comando:
```bash
cargo run --release
```

Este comando compila seu projeto Rust no modo release e inicia o bot de arbitragem com a configuração mais recente.

### Argumentos de Linha de Comando

Você pode passar vários argumentos de linha de comando para personalizar o comportamento do bot:

- `--config <path>`: Especifica um arquivo de configuração personalizado.
- `--verbose`: Habilita logs detalhados para fins de depuração.

Exemplo:
```bash
cargo run --release -- --config config.toml --verbose
```

## Uso

Siga as instruções no terminal para definir seus parâmetros de negociação. O bot monitorará continuamente oportunidades de arbitragem com base na sua configuração.

## Conceitos-Chave

### Flash Loans

Flash loans permitem que você tome empréstimos de ativos sem necessidade de garantia, desde que o valor emprestado seja devolvido dentro do mesmo bloco de transação. Esse mecanismo é essencial para executar estratégias de arbitragem de forma eficaz.

### Oportunidades de Arbitragem

O bot monitora continuamente os feeds de preços em diferentes exchanges para identificar oportunidades de negociação lucrativas. Quando uma discrepância de preço é detectada, ele executa uma compra em uma exchange e uma venda em outra.

### Smart Contracts

Os contratos inteligentes gerenciam a execução dos flash loans, garantindo que todas as transações sejam concluídas com sucesso dentro de um único bloco.

###⚠️ **Aviso Legal:** 

O uso deste projeto é por sua conta e risco. Não nos responsabilizamos por quaisquer danos, perdas ou consequências resultantes de sua utilização. 

