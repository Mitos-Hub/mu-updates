# Mu Zyon - Updates

Repositório de atualização do cliente Mu Zyon.

## Como adicionar um patch

1. Coloque o arquivo na pasta correta aqui no repositório (ex: `Data/Local/arquivo.bmd`)
2. Gere o MD5 no PowerShell:
   ```powershell
   (Get-FileHash 'caminho\arquivo.bmd' -Algorithm MD5).Hash.ToLower()
   ```
3. Adicione a entrada no `manifest.json`:
   ```json
   {
     "path": "Data/Local/arquivo.bmd",
     "url": "https://raw.githubusercontent.com/Mitos-Hub/mu-updates/main/Data/Local/arquivo.bmd",
     "md5": "cole_o_md5_aqui"
   }
   ```
4. Commit e push — o launcher vai baixar automaticamente na próxima vez que o jogador abrir.
