# NREduTech: Diagramas de Atividade

![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)
![Contexto](https://img.shields.io/badge/Contexto-TCC_(IFPR%20Campus%20Irati)-blue)
![Repositório Principal](https://img.shields.io/badge/Repositório-NREduTech_Código-lightgrey?logo=github)

Este repositório serve como um compêndio visual dos diagramas de atividade para o projeto **NREduTech**.

O projeto NREduTech é um "sistema Web voltado à gestão de componentes curriculares e recursos didáticos para o Núcleo Regional de Educação de Irati-PR e municípios vinculados". Este repositório documenta visualmente os fluxos de processo e regras de negócio implementadas.

O repositório principal do código-fonte pode ser encontrado em: [victorhjsantiago/nredutech](https://github.com/victorhjsantiago/nredutech).

---

## 📚 Fluxos do Sistema

Clique no título de um módulo para recolher ou expandir o diagrama de atividade correspondente.

<details open>
  <summary><strong>1. Módulo: Gestão de Escolas e Municípios</strong></summary>
  <p align="center">
    <br>
    <em>Fluxo restrito ao Administrador para gerenciar a infraestrutura base do sistema (RN-010). Inclui verificações de integridade para exclusão (RN-033, RN-034).</em>
    <br><br>
    <img src="images/diagrama_escolas_municipios.png" alt="Diagrama de Atividade: Gestão de Escolas e Municípios" width="80%">
  </p>
</details>

<details open>
  <summary><strong>2. Módulo: Gestão de Turmas</strong></summary>
  <p align="center">
    <br>
    <em>Fluxo de CRUD de turmas. Respeita o escopo de permissão de cada usuário (Admin vê tudo, Diretor/Professor veem apenas sua escola, RN-013) e verifica dependências (RN-015).</em>
    <br><br>
    <img src="images/diagrama_turmas.png" alt="Diagrama de Atividade: Gestão de Turmas" width="80%">
  </p>
</details>

<details open>
  <summary><strong>3. Módulo: Gestão de Disciplinas (Componentes Curriculares)</strong></summary>
  <p align="center">
    <br>
    <em>Fluxo de CRUD de disciplinas, incluindo o processo de aprovação (RN-038). Apenas Admins podem criar disciplinas "Globais" (RN-017).</em>
    <br><br>
    <img src="images/diagrama_disciplinas.png" alt="Diagrama de Atividade: Gestão de Disciplinas" width="80%">
  </p>
</details>

<details open>
  <summary><strong>4. Módulo: Gestão de Ofertas de Componentes</strong></summary>
  <p align="center">
    <br>
    <em>Processo de associação (vínculo) entre uma Turma, uma Disciplina e um Professor. Inclui regras de escopo (RN-020) e prevenção de duplicidade (RN-035).</em>
    <br><br>
    <img src="images/diagrama_ofertas_componentes.png" alt="Diagrama de Atividade: Gestão de Ofertas de Componentes" width="80%">
  </p>
</details>

<details open>
  <summary><strong>5. Módulo: Gestão de Recursos Didáticos</strong></summary>
  <p align="center">
    <br>
    <em>Fluxo de cadastro e manutenção do inventário. Inclui a lógica de cadastro em lote único ou em itens individuais (RN-039) e verificação de agendamentos (RN-023).</em>
    <br><br>
    <img src="images/diagrama_recursos_didaticos.png" alt="Diagrama de Atividade: Gestão de Recursos Didáticos" width="80%">
  </p>
</details>

<details open>
  <summary><strong>6. Módulo: Gestão de Usuários e Perfis</strong></summary>
  <p align="center">
    <br>
    <em>Diagrama composto que mostra 3 fluxos: 1) Registro público com status "Pendente" (RN-040); 2) Gestão de usuários pelo Admin/Diretor; 3) Auto-gestão de perfil pelo próprio usuário.</em>
    <br><br>
    <img src="images/diagrama_usuarios.png" alt="Diagrama de Atividade: Gestão de Usuários e Perfis" width="80%">
  </p>
</details>

<details open>
  <summary><strong>7. Módulo: Agendamento de Recursos e Laboratórios</strong></summary>
  <p align="center">
    <br>
    <em>Fluxo central do sistema. Detalha a reserva (com validações de conflito, RN-026) e o cancelamento (com regras de antecedência, RN-028).</em>
    <br><br>
    <img src="images/diagrama_agendamentos.png" alt="Diagrama de Atividade: Agendamento de Recursos" width="80%">
  </p>
</details>

<details open>
  <summary><strong>8. Módulo: Gerenciamento de Relatórios</strong></summary>
  <p align="center">
    <br>
    <em>Fluxo de geração e exportação de relatórios. Acesso restrito a Admins e Diretores (RN-043), com isolamento de dados por escola para Diretores (RN-030).</em>
    <br><br>
    <img src="images/diagrama_relatorios.png" alt="Diagrama de Atividade: Geração de Relatórios" width="80%">
  </p>
</details>

<details open>
  <summary><strong>9. Módulo: Configurações (Backup e Restore)</strong></summary>
  <p align="center">
    <br>
    <em>Fluxo de alta-segurança (restrito a Admins, RN-031) para realizar backups e restaurações do sistema, exigindo confirmação de senha (RN-044).</em>
    <br><br>
    <img src="images/diagrama_configuracoes.png" alt="Diagrama de Atividade: Configurações (Backup e Restore)" width="80%">
  </p>
</details>

---

<p align="center">
  Desenvolvido por <strong>Victor Henrique de Jesus Santiago</strong>.
  <br>
  <em>Baseado no TCC: "NREDUTECH: SISTEMA WEB PARA GESTÃO DE COMPONENTES CURRICULARES E DE RECURSOS DIDÁTICOS" (IFPR, 2025).</em>
</p>
