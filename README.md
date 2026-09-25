# Site da Dra. Maria Luiza Gutmacher

Site estático criado a partir da estrutura visual do [modelo My Odontologia](https://modelositeodonto.vercel.app/), com adaptação de marca, conteúdo e fotos públicas do [Instagram da doutora](https://www.instagram.com/dra.mariagutmacher/). A fonte Hanken Grotesk, a abertura `intro-camera.mp4`, o carrossel e o fluxo de agendamento foram preservados. A paleta usa creme, marrom escuro e cobre, inspirada nos retratos do perfil. No hero, `assets/hero-clareamento.mp4` reproduz em loop os primeiros 9 segundos do vídeo de clareamento ao lado do retrato da doutora, com um degradê suave entre os dois. Na seção Sobre, `assets/video-consultorio.mp4` é reproduzido localmente e começa automaticamente quando entra na tela, com controles para pausar ou retomar.

## Prévia local

Na pasta `C:\maluodonto`, execute um servidor estático, por exemplo:

```powershell
python -m http.server 4180
```

Abra `http://127.0.0.1:4180/`. Não abra `index.html` diretamente pelo explorador, pois alguns navegadores bloqueiam o carregamento dos quadros locais.

## Personalização

- `config.js`: Instagram, WhatsApp, endereço, avaliações, serviços e preferências de atendimento.
- `index.html`: textos, apresentação, animações e cores CSS.
- `assets/maria-*.webp`: fotos da doutora e conteúdo odontológico extraídos do Instagram e convertidos para WebP.
- `assets/intro-camera.mp4` e `assets/frames/`: animação preservada do modelo. `assets/hero-clareamento.mp4`: trecho de 9 segundos usado no hero.
- `privacy.html`: explicação do tratamento dos dados no agendamento.
- `vercel.json`: cabeçalhos de segurança para eventual hospedagem na Vercel.

O agendamento **não reserva um horário automaticamente**. O visitante escolhe serviço, dia e período; a solicitação é montada em uma mensagem para o WhatsApp da doutora. A confirmação depende da resposta dela. Como o horário de funcionamento não foi confirmado, ele não é exibido.

## Antes de publicar

Confirme com a cliente o endereço exato e autorização de uso das fotos. Confira o número de avaliações, que pode mudar. Teste WhatsApp, Instagram, avaliações e localização em um celular real. A pasta ainda não foi vinculada a um repositório nem publicada; o site original da My não foi alterado.

Dados e referências consultados em 25/09/2026 estão em [FONTES.md](FONTES.md). O guia de interface utilizado foi a skill [UI/UX Pro Max](https://github.com/mateusmon/skiiluxmax/tree/main/ui-ux-pro-max) indicada pelo usuário.
