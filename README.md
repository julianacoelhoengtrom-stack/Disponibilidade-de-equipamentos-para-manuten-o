# Aplicativo móvel — Visita Técnica EC

Este pacote contém somente a aplicação Android móvel. Os registros e assinaturas ficam salvos no próprio aparelho, sem depender de internet.

## O que o aplicativo faz

- Abre com uma ilustração de um técnico de Engenharia Clínica.
- Já seleciona o mês atual.
- Usa os setores da ronda e permite informar o equipamento.
- Permite selecionar Diego Gama ou Paulo Roberto.
- Registra nome e função de quem respondeu no setor.
- Mostra as áreas de assinatura em tela inteira.
- Salva a visita e o PDF no aparelho.
- Permite compartilhar o PDF ou o pacote JSON com os dados e PDFs para importar na aplicação web.

## Como colocar no GitHub

1. Crie um repositório GitHub vazio.
2. Envie o conteúdo desta pasta para a raiz do repositório, incluindo `.github/workflows/build-apk.yml`.
3. Abra a aba **Actions** do repositório e habilite os fluxos, se o GitHub pedir.
4. A cada envio que alterar `www/index.html` (ou outro arquivo do app), o GitHub gera um APK automaticamente.
5. Para gerar manualmente, abra **Actions → Gerar APK Android → Run workflow**.
6. Quando o processo terminar, abra a execução e baixe o artefato **APK-Visita-Tecnica-EC**.

O APK gerado é de depuração e pode ser instalado diretamente em aparelhos Android. Quando você trocar somente o HTML, não precisa alterar o workflow.

## Teste no computador

Abra `www/index.html` em um navegador moderno. A gravação offline, as visitas e a assinatura funcionam sem servidor. No navegador, os botões de arquivo baixam os arquivos; dentro do APK, eles abrem o menu nativo para compartilhar ou salvar.

## Arquivos principais

- `www/index.html`, `www/styles.css`, `www/app.js`: telas e comportamento do app.
- `www/assets/tecnico-abertura.png`: imagem de abertura.
- `res/icon.png` e `res/icon/android/`: ícone do aplicativo.
- `config.xml`: configuração Android/Cordova.
- `.github/workflows/build-apk.yml`: geração automática do APK.
