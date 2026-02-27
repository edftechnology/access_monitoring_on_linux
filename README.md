# Como configurar/instalar/usar o `Monitoramento de Acesso` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `Monitoramento de Acesso` no `Linux Ubuntu`.

## _Abstract_

_In this document are contained the main commands and settings to set up/install/use the `Access Monitoring` on `Linux Ubuntu`._


## Descrição [2]

### `Monitoramento de acesso`

O monitoramento de acesso é o processo de rastrear e registrar as atividades de usuários em sistemas de computador, redes ou recursos específicos. Isso inclui acompanhar quem acessa o sistema, quando e quais ações são realizadas. Essa prática é fundamental para garantir a segurança da informação, detectar comportamentos suspeitos ou não autorizados, e cumprir requisitos de conformidade regulatória. O monitoramento de acesso geralmente envolve a coleta e análise de logs, uso de ferramentas de segurança, como firewalls e sistemas de detecção de intrusões, e a implementação de políticas de acesso e controle de privilégios.


## 1. Como configurar/instalar/usar o `Access Monitoring` no `Linux Ubuntu` [1][3]

Para configurar/instalar/usar o `Access Monitoring` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```    

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando:
    ```bash
    sudo apt clean
    ```
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do `cache` local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando:
    ```bash
    sudo apt autoclean
    ```

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando:
    ```bash
    sudo apt autoremove -y
    ```

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt update
    ```

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes:
    ```bash
    sudo apt --fix-broken install
    ```

    2.6 Limpar o `cache` do gerenciador de pacotes `apt` novamente:
    ```bash
    sudo apt clean
    ```
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt list --upgradable
    ```

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt full-upgrade -y
    ```
    

Para verificar se alguém está tentando acessar seu computador no `Linux` através do `Terminal Emulator`, você pode usar várias ferramentas e comandos que fornecem informações sobre as conexões de rede, usuários logados e tentativas de _login_. Aqui estão algumas maneiras de fazer isso:

1. **`who`:** Mostra quem está logado no momento: `who`  

2. **`w`:** Exibe quem está logado e o que estão fazendo: `w`

3. **`last`:** Mostra um registro das últimas _logins_ no sistema. Pode ser útil para ver tentativas recentes de acesso: `last`

3. **`netstat`:** Fornece uma variedade de estatísticas de rede. Para ver conexões ativas, você pode usar: `netstat -tunapl`

-`-t` (TCP)

-`-u` (UDP)

-`-n` (Endereços como números)

-`-a` (Mostra todas as conexões)

-`-p` (Mostra o programa associado a cada conexão)

### 1.1 Para usuários de sistemas que usam o `ss` em vez do `netstat`:

1. **Verificar _logs_ do sistema:** Logs como `/var/log/auth.log` (em sistemas baseados em Debian) podem fornecer informações sobre tentativas de login e outras atividades de autenticação:

    ```bash
    sudo cat /var/log/auth.log
    ```

É importante manter o sistema atualizado e seguir as melhores práticas de segurança, como usar _firewalls_, alterar senhas regularmente e usar autenticação de dois fatores, se possível, para melhor proteger seu sistema contra acessos não autorizados.


### 1.2 Código completo para configurar/instalar

Para configurar/instalar o `auditd` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Digite o seguinte comando e pressione `Enter`:

    ```bash
    NÃO há.
    ```
    

## Referências

[1] OPENAI. ***Instalar o `monitoramento de acesso` no `linux ubuntu` pelo `terminal emulator`.*** Disponível em: <https://chat.openai.com/c/7772a507-88e7-46c8-ad7a-64a2d9011843> (texto adaptado). ChatGPT. Acessado em: 21/02/2024 12:00.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). ChatGPT. Acessado em: 21/02/2024 12:00.

