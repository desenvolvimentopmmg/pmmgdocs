
# QAPP - REGISTRO DE ALTERAÇÕES (Change Log)

Todas as mudanças notáveis deste projeto serão documentadas abaixo.

## [Versão 1.2.20] - 17/02/2023
 
### Recursos adicionados
   
- Adição do card "Carnaval"

## [Versão 1.2.7] - 10/01/2023
 
### Recursos adicionados

- Patrulha Rural: Adição do cadastro de Animas nos Endereços Rurais
   
### Recursoso alterados

- Patrulha Rural: Ajustes, melhoramentos e alterações requisitadas pelos responsáveis pela Patrulha Rural
- Patrulha Rural: Otimizações no mecanismo de sincronização dos dados

## [Versão 1.2.4] - 23/12/2022
 
### Recursos adicionados

- Adição do card "Brasil M.A.I.S." para redirecionamento ao [link](https://plataforma-pf.sccon.com.br/#/), para usuários das unidades CPMAMB, BPMAMB, CTS e DTS.

## [Versão 1.2.0] - 01/12/2022

### Segurança

- Detecção, registro e bloqueio de dispositivos classificados como Emuladores ou "Rooteados".

Pretende-se com a adição desse recurso identificar usuários que utilizam o app em dispositivos suspeitos ou que não ofereçam segurança para os dados compartilhados entre os serviços da PMMG e o dispositivo do usuário. Essa atualização não apresenta nenhuma modificação aparente.
 
## [Versão 1.1.3] - 21/11/2022
 
### Recursos adicionados

- Botão de redirecionamento para o Helios Web no menu superior da tela do Helios no aplicativo
   
### Correções

- Atualização das bibliotecas de recebimento de notificação no Android

Foram detectados alguns problemas em alguns aparelhos Android correspondentes a issue descrita nesses links: [LINK 1](https://github.com/firebase/flutterfire/issues/9446), [LINK 2](https://github.com/firebase/flutterfire/pull/9494)

Com a atualização das bibliotecas e realização de alguns ajustes no código fonte, esse problema, até onde foi testado, fica resolvido.
 
## [Versão 1.1.0] - 27/10/2022
 
### Recursos adicionados

- Mecanismo de verificação de nova versão do aplicativo (Android)

Caso a verificação encontre uma nova versão do app disponível, ele informará o usuário e caso o usuário concorde, realizará o download e a atualização do app sem a necessidade de entrar na PlayStore. Esperasse com esse mecanismo que o usuário realize a atualização do app para a versão mais recente mais rapidamente.

- Novo card de OS (Atendimento) para militares do CTT

### Segurança

- Aprimoramento de segurança: Troca da chave de aplicação para o login

Utilização da nova chave de autenticação do QApp, para que a chave anterior seja desativada no próximo mês. A utilização desta nova chave também faz com que o aplicativo obtenha o novo token de aplicação com expiração de 14 dias (o token anterior obtido no PMSSO tinha validade infinita) e permite que o mecanismo de refresh token seja utilizado.

- Aprimoramento de segurança: Refresh token

Mecanismo de atualização do token de autenticação do aplicativo quando este token expira. Este novo fluxo foi implementado no PMSSO e o QApp é a primeira aplicação a fazer uso dele.

- Aprimoramento de segurança: Criptografia de dados sensíveis armazenados no app

Adicionamos a criptografia de dados sensíveis armazenados na aplicação como o Token de autenticação e o Refresh Token. Anteriormente estes dados poderiam ser acessados indevidamente caso o dispositivo fosse "roteado" pelo usuário. Agora, mesmo que o usuário realize o root do aparelho, os dados obtidos estarão criptografados.
 