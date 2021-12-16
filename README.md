#### mysql backup, edit crontab
(crontab -l 2>/dev/null; echo "0 2 * * * /root/Mysql_backup/mysqlbu.sh" >/dev/null 2>&1") | crontab -
