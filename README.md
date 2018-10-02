accel-ppp-webif-fork Por Luciano de Sousa Castro
===============

accel-ppp web interface (web2.0, ajax, other buzzwords)

IMPORTANTE!

Depois de instalado gerar a senha: 

#php data.php --password suasenha

Copie a saida do comando a cima e substitua linha equivalente dentro de  data.php.

Na linha 57 do arquivo index.php coloque o ip do servidor do onde está rodando o tailon. (tailon é usando pra ler os logs do accel.)

Para o correto funcionamento do fork você precisa usar a linha abaixo no modulo "[cli]", essa linha vai dentro do arquivo /ete/accel-ppp.conf, com base nessa ordem vai ser montada as colunas na interface web.

sessions-columns=ifname,username,ip,ip6,ip6-dp,type,state,uptime,calling-sid,rate-limit,rx-bytes,tx-bytes

INSTALAÇÃO DO TAILON!
A instalação do tailon é muito fácil é só descompactar 

#tar -vzxf tailon_1.0.0_linux_amd64.tar.gz

Dar permissão de execução 

#chmod +x tailon

E ativar a iniciação dele no /etc/rc.local com a seguinte linha 

/root/tailon /var/log/accel-ppp/*

Pronto acho que é só a se acharem algum erro me avisem, basicamente é isso!




