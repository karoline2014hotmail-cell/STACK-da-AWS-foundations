# STACK-da-AWS-foundations 

Implementar sua primeira stack com AWS CloudFormation é uma excelente forma de começar a gerenciar infraestrutura como código na AWS. Aqui está um passo a passo simplificado para te guiar:
🚀 Etapas para criar sua primeira stack
1. Acesse o Console da AWS
• 	Vá para o AWS Management Console.
• 	Faça login com sua conta da AWS.
2. Configure permissões
• 	Certifique-se de que seu usuário tem permissões adequadas via IAM (Identity and Access Management).
• 	Você pode usar políticas gerenciadas como  ou criar uma política personalizada.
3. Crie um template CloudFormation
• 	O template define os recursos que serão criados. Exemplo básico em YAML:

CÓDIGO:
AWSTemplateFormatVersion: '2010-09-09'
Description: Minha primeira stack
Resources:
  MeuBucketS3:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: meu-primeiro-bucket-cloudformation

5. Implante a stack
• 	No console do CloudFormation, clique em "Create stack" > "With new resources (standard)".
• 	Escolha "Upload a template file" e envie seu arquivo YAML.
• 	Dê um nome à stack e clique em "Next" até chegar em "Create stack".
6. Monitore o progresso
• 	Acompanhe o status da stack no console. Quando estiver como , seus recursos foram criados com sucesso.
7. Verifique os recursos
• 	Vá até o serviço correspondente (como S3) e confirme que o recurso foi criado.


O Amazon CloudWatch é o serviço de monitoramento e observabilidade da AWS que permite acompanhar, em tempo real, o desempenho e a integridade dos seus recursos e aplicações na nuvem. Ele funciona como o "centro nervoso" da sua infraestrutura na AWS.
🔍 Principais funcionalidades do CloudWatch
• 	Coleta de métricas: Monitora automaticamente serviços da AWS como EC2, RDS, Lambda, S3, entre outros.
• 	Alarmes: Permite configurar alertas com base em métricas (ex: uso de CPU acima de 80%).
• 	Dashboards personalizados: Visualize métricas e logs em painéis interativos.
• 	Logs e eventos: Armazena e analisa logs de aplicações e eventos do sistema.
• 	Automação de ações: Pode acionar funções Lambda, enviar notificações ou escalar recursos automaticamente com base em condições definidas.
📦 Exemplos de uso
• 	Monitorar a saúde de instâncias EC2.
• 	Detectar falhas em aplicações com logs centralizados.
• 	Criar alarmes para evitar estouros de custo ou sobrecarga de recursos.
Você pode explorar mais detalhes na documentação oficial da AWS.

O AWS CloudTrail é um serviço essencial para auditoria e segurança na AWS, pois permite rastrear e registrar todas as ações realizadas em sua conta. Aqui estão os principais fundamentos:

🔐 O que é o AWS CloudTrail?
O CloudTrail registra eventos relacionados a chamadas de API feitas por usuários, serviços ou ferramentas na sua conta AWS. Isso inclui ações feitas via:
• 	Console da AWS
• 	AWS CLI
• 	SDKs da AWS
• 	Serviços automatizados
Esses registros são armazenados como arquivos JSON em buckets do Amazon S3, podendo ser analisados para fins de auditoria, segurança e conformidade.

🧭 Principais benefícios
• 	Auditoria de segurança: Identifique quem fez o quê, quando e de onde.
• 	Detecção de atividades suspeitas: Combine com Amazon CloudWatch para gerar alertas.
• 	Conformidade regulatória: Ajuda a atender requisitos como HIPAA, PCI-DSS, ISO 27001.
• 	Análise forense: Investigue incidentes de segurança com trilhas detalhadas.
• 	Governança de conta: Monitore alterações em configurações, permissões e recursos.

🛠️ Boas práticas de uso
• 	Habilite o CloudTrail em todas as regiões para garantir cobertura completa.
• 	Centralize os logs em uma conta dedicada de auditoria.
• 	Proteja os logs com políticas de IAM e criptografia.
• 	Integre com AWS Config e CloudWatch para monitoramento contínuo e automação de respostas.


