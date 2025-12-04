
## 🌟 Status do Banco de Dados: Modelagem Lógica Concluída ##
"Monitorando o pulso da cidade: veículos, rotas e eventos em tempo real."

## 💡 Sobre o Projeto 💡 ## 

Este repositório apresenta a Modelagem Lógica de Dados para o UrbanPulse, uma plataforma avançada de Gestão de Mobilidade Urbana. O sistema é desenhado para unificar dados de frotas de transporte com informações de sensores IoT (Internet of Things), possibilitando o rastreamento detalhado de viagens, a identificação e registro de incidentes, e a aplicação de um sistema de tarifação inteligente e dinâmica.

## 🧠 Arquitetura e Pilares de Dados ## 
A arquitetura do banco de dados é fundamentada em três pilares interconectados que garantem a gestão completa do ecossistema de transporte urbano.

1. **🚌 Frota e Logística**

Este pilar foca no Gerenciamento Físico e Operacional dos ativos de transporte.

VEICULO: Cada veículo é rastreado individualmente, identificado por sua Placa e pelo seu Status operacional (em serviço, manutenção, etc.).

ROTA: Define os trajetos pré-determinados, incluindo informações cruciais como a distância total e o tempo estimado de percurso.

2. **📡 Monitoramento IoT (Internet of Things)**

Esta camada introduz a Inteligência em Tempo Real, capturando e processando dados ambientais e operacionais.

SENSOR: Detalha os dispositivos de hardware acoplados aos veículos.

EVENTO_MOBILIDADE: Registra todos os incidentes em tempo real (e.g., congestionamento, acidentes, falhas mecânicas). Esses eventos são detectados e comunicados diretamente pelos sensores.

3. **👤 Usuários e Operação**

Este pilar gerencia o Controle de Acesso, a Tarifação e o registro histórico do uso do sistema.

USUARIO & TIPO_USUARIO: Permite um sistema de Tarifação Segmentada (e.g., Estudante, Idoso, Comum), onde diferentes grupos utilizam a Tabela de Tarifas para calcular o custo da viagem.

VIAGEM: O registro histórico central que conecta todos os dados: quem usou (Usuário), o que usou (Veículo/Rota), e as coordenadas tempo-espaciais (quando e onde).

