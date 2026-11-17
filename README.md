# Teste Técnico – Infraestrutura de TI

## Objetivo
Avaliar os conhecimentos do candidato em **segurança da informação** e **redes de computadores**, por meio de um questionário dissertativo e de um desafio prático no **Cisco Packet Tracer**.

---

## Instruções

O teste tem duas partes:

1. **Questionário de segurança** – 5 questões dissertativas
2. **Desafio no Packet Tracer** – montar e configurar uma pequena rede

- Responda às questões com suas próprias palavras. **Explicar o raciocínio vale mais do que respostas curtas.**
- Se não souber resolver alguma parte, siga para a próxima e **anote o que tentou**.
- O enunciado também está disponível em PDF (`Teste_Admissao_TI.pdf`), caso prefira imprimir ou ler por lá.

---

## Parte 1 – Questionário de segurança

Responda às cinco questões no arquivo **`respostas.md`**, que está neste repositório.

### Questão 1 – Phishing
Um colaborador recebe um e-mail que parece ser do banco da empresa, dizendo que a conta será bloqueada em 24 horas se ele não confirmar seus dados pelo link enviado. Quais sinais indicam que pode ser um golpe, e o que você orientaria esse colaborador a fazer?

### Questão 2 – Autenticação multifator
O que é autenticação multifator (MFA)? Explique por que ela protege a conta mesmo quando a senha do usuário é descoberta por outra pessoa.

### Questão 3 – Tipos de malware
Explique a diferença entre vírus, ransomware e spyware.

### Questão 4 – HTTP e HTTPS
Qual a diferença entre HTTP e HTTPS? Se um site aparece com o cadeado no navegador, isso garante que ele é confiável? Justifique.

### Questão 5 – Acesso remoto a equipamentos
Por que não se deve usar Telnet para administrar remotamente roteadores e switches? O que deve ser usado no lugar?

---

## Parte 2 – Desafio no Packet Tracer

A empresa tem dois setores: **Administrativo** e **Técnico**. Cada setor tem um switch e dois computadores, e os dois switches estão ligados a um roteador. Ao final, **todos os PCs devem conseguir se comunicar entre si**, inclusive entre setores diferentes.

> O Cisco Packet Tracer é gratuito e pode ser baixado após um cadastro no [Cisco Networking Academy](https://www.netacad.com/cisco-packet-tracer).

### Equipamentos
- 1 roteador Cisco 2911
- 2 switches Cisco 2960 (um por setor)
- 4 PCs (dois por setor)

### Plano de endereçamento

| Equipamento | Interface | Endereço IP | Máscara | Gateway |
| --- | --- | --- | --- | --- |
| Roteador | G0/0 (Administrativo) | 192.168.10.1 | 255.255.255.0 | — |
| Roteador | G0/1 (Técnico) | 192.168.20.1 | 255.255.255.0 | — |
| PC-ADM-1 | NIC | 192.168.10.10 | 255.255.255.0 | 192.168.10.1 |
| PC-ADM-2 | NIC | 192.168.10.11 | 255.255.255.0 | 192.168.10.1 |
| PC-TEC-1 | NIC | 192.168.20.10 | 255.255.255.0 | 192.168.20.1 |
| PC-TEC-2 | NIC | 192.168.20.11 | 255.255.255.0 | 192.168.20.1 |

### Tarefas
1. Faça o cabeamento entre os equipamentos.
2. Configure o hostname do roteador como **R-SCOT** e dos switches como **SW-ADM** e **SW-TEC**.
3. Configure as interfaces do roteador e os endereços IP dos PCs conforme a tabela.
4. Salve a configuração do roteador e dos switches.
5. Teste a comunicação com `ping` entre um PC do Administrativo e um PC do Técnico.
6. Salve o arquivo do Packet Tracer (`.pkt`) com o seu nome.

---

## O que esperamos
- Respostas claras e com raciocínio explicado
- Rede funcionando conforme o plano de endereçamento
- Configurações salvas nos equipamentos
- Um passo a passo explicando o que foi feito e como validar

---

## Critérios de avaliação
- Domínio dos conceitos de segurança da informação
- Clareza na comunicação das respostas
- Cabeamento e configuração corretos
- Comunicação entre os setores funcionando
- Organização e capacidade de documentar o trabalho

---

## Diferenciais
- Configurar acesso remoto seguro (SSH) no roteador
- Proteger o acesso aos equipamentos com senhas (`enable secret`, console)
- Adicionar descrições nas interfaces (`description`)
- Configurar um banner de aviso (`banner motd`)

---

## Observações
- É permitido consultar a internet durante o teste
- Não há cronômetro: organize seu tempo dentro do prazo de entrega

---

## Entrega

Envie sua solução em um arquivo **.zip** para **at@scotconsultoria.com.br** em até **10 dias corridos** após o recebimento do teste.

- **Assunto do e-mail:** `Teste Infra – Seu Nome`
- **Nome do arquivo:** `teste-infra-seu-nome.zip`

### O .zip deve conter
- **`respostas.md`** preenchido com as respostas da Parte 1 (também aceitamos `.docx` ou `.pdf`)
- O arquivo do Packet Tracer: **`seu-nome.pkt`**
- Um arquivo **`README.md`** com:
  - Versão do Packet Tracer utilizada
  - Passo a passo do que foi feito na Parte 2
  - Como validar que a rede está funcionando (ex.: quais `ping` executar)
  - O que não conseguiu concluir e o que tentou, se for o caso
- (Opcional) Prints do `ping` bem-sucedido entre os setores

> Se o arquivo passar de 20 MB, envie um link de download (Google Drive, WeTransfer etc.).

---

Em caso de dúvidas, envie um e-mail para **at@scotconsultoria.com.br**

**Boa sorte! 🚀**
