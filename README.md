# AWS CloudFormation 🏗️☁️

O **AWS CloudFormation** é um serviço da AWS que permite **modelar, provisionar e gerenciar recursos de infraestrutura** de forma automatizada, segura e replicável, usando o conceito de **Infraestrutura como Código (IaC)**.

---

## 📘 Conceito

Com o CloudFormation, você define sua infraestrutura em arquivos de modelo ou templates que podem ser escritos em **YAML** ou **JSON**. Esses arquivos descrevem os recursos da AWS que você deseja criar, como:

- Instâncias EC2
- Buckets S3
- Grupos de segurança
- Funções Lambda
- Bancos de dados RDS

O serviço interpreta esse modelo e cria uma **stack** , que é um conjunto de recursos gerenciados como uma única unidade.

---

## ⚙️ Componentes Principais

| Componente        | Descrição                                                                 |
|-------------------|---------------------------------------------------------------------------|
| **Template**       | Documento YAML/JSON que define os recursos e configurações desejadas     |
| **Stack**          | Conjunto de recursos criados a partir de um template                     |
| **Change Set**     | Prévia das alterações antes de atualizar uma stack                       |
| **Drift Detection**| Verifica se os recursos foram modificados fora do CloudFormation         |
| **Nested Stacks**  | Permite reutilizar templates dentro de outros templates                  |

---

## ✅ Benefícios

- **Automação Total**: 
Criação e atualização de ambientes com um único comando
- **Consistência**:
 Evita erros manuais e garante ambientes idênticos
- **Controle de Versão**: 
Fácil rastreamento de mudanças na infraestrutura
- **Auditoria e Conformidade**: 
Integração com AWS Config e CloudTrail
- **Escalabilidade**: 
Ideal para ambientes multi-conta e multi-região

---

## 📦 Exemplo de Template YAML

```yaml
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  MeuBucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: fernanda-bucket-exemplo

```
## 🔬Experiência 

Inicialmente tive algumas dificuldades mas após algumas tentativas consegui rodar os três exemplos da aula, de fato é muito prático provisionar uma infraestrutura via CloudFormation e toda a aula foi interessante para desmistificar a impressão que temos que gerar servidores ou instâncias por JSON ou YAML pode ser dificil.

## 🔎 Conclusão

Esta ferramenta me despertou mais uma grande curiosidade sobre o que mais podemos fazer com a AWS, têm sido notável que este serviço tem muitos recursos que ajudam alguém iniciante à provisionar uma estrutura responsiva de forma prática e segura, os modelos que a AWS disponibiliza para a criação de stacks são de fácil compreensão e compatíveis com diversas demandas.
