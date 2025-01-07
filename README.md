Gema Token (GEM)

Este repositório contém o contrato inteligente para o token Gema (símbolo: GEM), desenvolvido em Solidity e baseado no padrão ERC20. O contrato utiliza bibliotecas da OpenZeppelin para garantir segurança e boas práticas.

Descrição

Gema é um token ERC20 com os seguintes recursos adicionais:

    Minting: O proprietário pode criar novos tokens.
    Burning: Qualquer titular pode queimar seus próprios tokens.
    Permit (EIP-2612): Suporte para assinatura off-chain para aprovações de transferências.
    Controle de propriedade: Apenas o proprietário pode realizar ações administrativas, como criar novos tokens.

Funcionalidades

    ERC20:
        Nome do token: Gema
        Símbolo: GEM
        Decimais: 18 (padrão ERC20)

    Burnable:
        Qualquer titular pode queimar (burn) seus próprios tokens.

    Mintable:
        Apenas o proprietário pode cunhar (mint) novos tokens.

    Permit (EIP-2612):
        Permite aprovações de transferências através de assinaturas fora da cadeia.

    Controle de propriedade:
        O contrato utiliza Ownable para definir o controle do proprietário, permitindo que apenas o proprietário execute certas funções administrativas.

Instalação

Certifique-se de que você tenha o framework de desenvolvimento Solidity (por exemplo, Hardhat ou Truffle) configurado.

    Clone o repositório:

git clone <https://github.com/alanrodrigofreitas/GemaToken>
cd <GemaToken>

Instale as dependências:

npm install

Compile os contratos:

    npx hardhat compile

Uso

Implantação

    Configure o endereço do proprietário inicial no script de implantação.
    Execute o script de implantação:

    npx hardhat run scripts/deploy.js --network <polygon>

Métodos principais

    Mint tokens: O proprietário pode cunhar novos tokens para um endereço:

mint(address to, uint256 amount)

Burn tokens: Qualquer titular pode queimar seus tokens:

    burn(uint256 amount)

    Aprovação via assinatura (Permit): Utiliza EIP-2612 para aprovar transferências com assinatura fora da cadeia.

Dependências

    OpenZeppelin Contracts ^5.0.0

Licença

Distribuído sob a Licença MIT. Veja LICENSE para mais informações.