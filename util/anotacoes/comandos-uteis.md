# Comando para testar a configuração dos beats se está funcionandno
metricbeat test config

# Comando para ativar senhas no elasticsearch
bin/elasticsearch-setup-passwords interactive

# Comando para verificar conexão do elasticsearch
curl -u elastic:'senha_atual' http://192.168.1.110:5601

# Cenários possíveis de uso 
# Quando usar cada opção:

# Enviando as métricas direto ao Elasticsearch
Elasticsearch (direto): Se você deseja simplicidade e velocidade sem manipulação dos dados, essa é a escolha ideal.

# Enviando ao logstash
Logstash: Se seu ambiente requer maior flexibilidade, capacidade de manipular dados ou já usa o Logstash para outros fins, essa opção é recomendada.

# Comando para passar dados de um volume para outro
docker run --rm -it   -v elk-stack_esdata:/old_data   -v esdata:/new_data   alpine sh -c "cp -a /old_data/. /new_data/"

# O alpine é um container temporário que é criado somente para a transferência de dados entre os volumes.