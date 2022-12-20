# rlone-sync-backup-auto
Faça backup/sync de arquivos de alguma aplicação para uma nuvem usando o rclone de forma automática.

Esse script executa uma ação no rclone.

# Como automatizar o uso?

Baixe o script na sua vps ou maquina local usando o wget

```bash
wget https://raw.githubusercontent.com/PA1NK1LL3R-777/rlone-sync-backup-auto/main/rclone-auto.sh
```

# Edite essas linhas:

```bash
DIR_ORIGEM="/home/user/Backup/" # <-- Altere seu diretório de origem (Os arquivos que vão ser backupados)

DIR_DESTINO="mydrive:/"          # <-- Altere seu dispositivo remoto (Para aonde vai)
```

# De permissão de execução para o script

```bash
chmod +x rclone-sync.sh  
```

# Mova para algum diretorio mais especifico

Exemplo:

```bash
mv -v rclone-auto.sh /usr/local/sbin/
```

# Agende no crontab para que possa ser executado automaticamente em X horas/minutos.

Entre em modo root, caso não já esteja.

```bash
sudo su -
```

Agora adcione a linha no crontab

```bash
crontab -e
```

Você vai escolher a quantidade de vezes que o backup será feito, exemplo:

```bash
00 14 * * * /usr/local/sbin/backup-completo.sh
```

Nesse exemplo, o backup será feito uma vez por dia, as 2:00/14:00 PM.

Aconselho que pesquise como usar o crontab, assim você saberá como configurar da melhor forma que vá lhe atender.
