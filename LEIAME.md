# Gangue Battle – passo a passo

## 1. Servidor (Firebase, grátis, sem programar servidor)
1. Acesse console.firebase.google.com > Criar projeto.
2. Menu "Realtime Database" > Criar banco > modo de teste.
3. Em Configurações do projeto > Seus apps > Web (</>) > copie o objeto firebaseConfig.
4. Cole os valores em `www/index.html`, no bloco `FIREBASE_CONFIG` (confira se `databaseURL` veio preenchido).

## 2. GitHub gera o APK
1. Crie um repositório no GitHub e envie TODOS estes arquivos (inclusive a pasta oculta .github).
2. Aba Actions > "Build APK" > aguarde ~5 min.
3. Clique na execução > Artifacts > baixe `gangue-battle-apk`, extraia e instale o .apk no celular.
4. Cada vez que você editar e der push, um novo APK é gerado.

## Segurança
- Login só por nome (NITRO / MAV), sem senha. Para o grupo de 2 pessoas serve, mas quem souber o nome entra.
- O modo de teste do Firebase expira em 30 dias: depois, troque as regras para `{"rules":{".read":true,".write":true}}` (aberto) ou peça para adicionarmos Firebase Auth com senha.
