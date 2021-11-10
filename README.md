# linuxmint-cinnamon
Melhorando a performance no linux mint

# Observação
Todas as dicas são reversiveis, então faça um backup dos arquivos que você alterar

# Primeira dica
 - cat /proc/sys/vm/swappiness
 - por padrão é 60
 - xed admin:///etc/sysctl.conf
 - ele vai pedir sua senha root duas vezes e logo depois abrira o arquivo sysctl.conf
 - vá até o final do arquivo e coloque a linha vm.swappiness=20
 - reinicie o computador
 - rode o comando cat /proc/sys/vm/swappiness

# Segunda dica
 - xed admin:///etc/default/grub
 - ele pedira sua senha root
 - procure pela linha GRUB_CMDLINE_LINUX
 - provavelmente estara vazio
 - coloque entra as aspas esse valor zswap.max_pool_percent=40
 - resultado GRUB_CMDLINE_LINUX="zswap.max_pool_percent=40"
 - rode sudo update-grub

# Terceira dica
 - O libreoffice utiliza recursos do java para algumas ações especificas
 - para desabilitar o java abra o libreoffice writer
 - va em ferramentas > opções > LibreOffice > avançado
 - Em opções java desmarca a "Utilizar um JRE"
 - aperte OK

# Quarta dica
 - abra os aplicativos de inicialização
 - desabilite "Relatórios do sistema"
 - desabilite "mintwelcome"
 - desabilite "Gerenciador de Atualizações"
 - caso você não tenha impresora desabilite "Print Queue Applet" ou "Miniaplicativo de fila de impressão"
 - se sua placa de video não for NVIDIA desabilite "Support for NVIDIA Prime"

# Quinta dica
 - desabilitar efeitos do sistema
 - va no menu > preferencias > efeitos
 - desabilite todas as opções

# Sexta dica
 - procure por "janelas em mosaico" no menu
 - desabilitar a opção