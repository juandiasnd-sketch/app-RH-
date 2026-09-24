# Nauber - Controle de Entrega de EPI

Versão sem tela de login no acesso normal.

## Como funciona
- O aplicativo abre normalmente, sem pedir e-mail e senha.
- O Firebase Authentication usa login Anônimo em segundo plano apenas para permitir acesso ao Firestore conforme as regras atuais.
- O Painel Administrativo continua protegido por e-mail e senha do Firebase Authentication.
- Fotos e assinaturas continuam armazenadas no Firestore como Base64; não usa Firebase Storage.

## Passo obrigatório no Firebase
No Firebase Console:
1. Authentication > Método de login.
2. Ative o provedor **Anônimo**.
3. Mantenha também **E-mail/senha** ativado para o Painel Admin.

## Firestore Rules
As regras podem continuar exigindo `request.auth != null`, pois o acesso normal será autenticado anonimamente em segundo plano.


## Importante
Ative o provedor Anonymous em Firebase Authentication. Nao e necessario criar login visivel para os usuarios do app.
