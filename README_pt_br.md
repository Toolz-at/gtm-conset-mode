
# Consent Mode Banner Template

Este repositório contém o template de Consent Mode Banner para o Google Tag Manager (GTM), utilizando a ferramenta gratuita disponibilizada por [Toolz](https://toolz.at).

## Descrição

O template implementa funcionalidades para gerenciar estados de consentimento do usuário, configurar modos de consentimento padrão e injetar o script necessário para exibir o banner de consentimento.

## Funcionalidades

- Configuração do estado de consentimento padrão.
- Armazenamento de informações de consentimento no `localStorage`.
- Integração com o Google Tag Manager.
- Injeção de scripts dinamicamente com permissões verificadas.
- Gerenciamento granular de categorias de consentimento:
  - **Necessário**: `functionality_storage`, `security_storage`.
  - **Marketing**: `ad_storage`, `ad_user_data`, `ad_personalization`.
  - **Analytics**: `analytics_storage`.
  - **Preferências**: `personalization_storage`.

## Dependências

- Biblioteca [Consent Management Platform](https://consentmodebanner.com).

## Estrutura do Código

O arquivo principal contém as seguintes funções e métodos:

- **`setDefaultConsentState`**: Define o estado de consentimento padrão.
- **`updateConsentState`**: Atualiza o estado de consentimento conforme a interação do usuário.
- **`getCookieValues`**: Obtém valores dos cookies relacionados ao consentimento.
- **`gtagSet`**: Configurações opcionais do Google Analytics, como:
  - `ads_data_redaction`
  - `url_passthrough`
  - `developer_id`
- **`queryPermission`**: Verifica permissões antes de executar a injeção do script.
- **`injectScript`**: Injeta o script do banner de consentimento.

## Como Configurar

1. Faça o download do código deste repositório.
2. Substitua os valores de exemplo no código pelas suas configurações específicas.
   - Configure `data.consetModeID` com o ID do seu banner.
3. Certifique-se de que as funções e bibliotecas requeridas estão devidamente configuradas no seu ambiente GTM.
4. Suba o script no Google Tag Manager como um template de tag customizada.

## Como Utilizar

- O script inicializa automaticamente ao ser carregado no GTM.
- Verifica o estado de consentimento atual e aplica as configurações padrão.
- Caso não haja consentimento armazenado, define os estados de consentimento conforme a configuração.

## Referências

Para mais informações, consulte a documentação oficial em [Consent Mode](https://consentmodebanner.com).

---

**Nota**: Este projeto foi desenvolvido como uma solução gratuita para gerenciar consentimentos no GTM. Contribuições são bem-vindas.
