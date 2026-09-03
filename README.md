# gil-papa.github.io

Site público do app **TCG Condition**. Publicado em <https://gil-papa.github.io/>.

Este repositório existe por duas exigências de fora:

- a **Play Store** pede a política de privacidade numa URL pública e estável — um link quebrado é
  motivo de reprovação numa revisão futura, meses depois da aprovação;
- o **AdMob** procura o `app-ads.txt` na raiz do domínio declarado no perfil de desenvolvedor.

O repositório do app é privado e continua privado. Aqui só mora o que precisa ser público.

## Não edite estes arquivos aqui

`index.html`, `privacidade.html` e `app-ads.txt` são **gerados**. A fonte da política é
`tcg-card-condition-plans/loja/politica-de-privacidade.md`, no repositório do app, e o gerador é
`tools/site/build_site.py`. Uma edição feita aqui some na próxima publicação — e, pior, faz a
política publicada divergir do que o app declara no Data Safety, que é motivo de suspensão e não
de correção.

Para publicar uma mudança:

```bash
cd ~/Desenvolvimento/tcg && python3 tools/site/build_site.py
cp tools/site/out/* ~/Desenvolvimento/gil-papa.github.io/
cd ~/Desenvolvimento/gil-papa.github.io && git add -A && git commit && git push
```

O Pages republica sozinho em um ou dois minutos.
