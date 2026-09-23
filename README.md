# Nauber - Controle de Entrega de EPI

Versao preparada para Git + Firebase sem Firebase Storage.

## Servicos usados
- Firebase Authentication (E-mail/Senha): acesso ao sistema.
- Cloud Firestore: colaboradores, equipamentos, estoque, historico, fotos e assinaturas.
- Firebase Hosting: opcional.

## Importante
As fotos sao comprimidas no navegador e salvas no Firestore como Data URL/Base64. O app limita imagens grandes para evitar ultrapassar o limite por documento do Firestore.

O sistema exige login antes de carregar dados. Somente crie usuarios autorizados em Firebase Authentication > Users.

## Publicar regras
No terminal, com Firebase CLI configurado:

```bash
firebase deploy --only firestore:rules
```

Ou copie o conteudo de `firestore.rules` para Firestore > Regras no Firebase Console e clique em Publicar.

## Hospedagem opcional

```bash
npm install -g firebase-tools
firebase login
firebase init hosting
firebase deploy
```
