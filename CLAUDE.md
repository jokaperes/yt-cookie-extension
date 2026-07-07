# yt-cookie-extension

@README.md

## Notas operacionais

- Extensão Chrome/Edge que exporta cookies do YouTube em formato Netscape para o yt-dlp. Par do projeto `/root/yt-transcript`.
- Branch de trabalho: `main`. Repo privado `jokaperes/yt-cookie-extension`. Sempre commitar E dar push.
- `/root/yt-cookie-extension-pack/` é um espelho usado só como staging do zip de release — não desenvolver lá; replicar mudanças a partir daqui.
- O yt-dlp (engine >= 2.3.3 do yt-transcript) rotaciona os cookies e os regrava no arquivo. Quando os cookies queimam, o fix é exportar de novo em janela anônima com conta reserva usando a extensão v1.1.
