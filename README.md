﻿# Calculadora de IP

Uma aplicação Spring Boot que fornece funcionalidades de cálculo de endereços IP, incluindo endereço de rede, endereço de broadcast, número de hosts, notação CIDR e determinação da classe de rede.

## Funcionalidades

- Cálculo do endereço de rede a partir do IP e máscara de sub-rede
- Cálculo do endereço de broadcast
- Determinação do número de hosts disponíveis
- Cálculo da notação CIDR
- Identificação da classe de rede (A, B, C, D ou E)

## Stack Tecnológica

- Java
- Spring Boot
- Maven

## Estrutura do Projeto

```
src/main/java/com/example/ipcalculator/
├── IpCalculatorApplication.java    # Classe principal da aplicação
├── controller/
│   └── IpCalculatorController.java # Controlador REST para cálculos de IP
└── service/
    └── IpCalculatorService.java    # Lógica de negócio para cálculos de IP
```

## Endpoints da API

### Calcular Informações de IP
- **URL**: `/calculate`
- **Método**: `POST`
- **Parâmetros**:
  - `ipAddress`: Endereço IP (ex: "192.168.1.1")
  - `subnetMask`: Máscara de sub-rede (ex: "255.255.255.0")
- **Resposta**: Objeto JSON contendo:
  - `networkAddress`: Endereço de rede calculado
  - `broadcastAddress`: Endereço de broadcast calculado
  - `numberOfHosts`: Número de hosts disponíveis
  - `cidr`: Notação CIDR
  - `networkClass`: Classe da rede (A, B, C, D ou E)

## Compilando o Projeto usando Docker

1. Clone o repositório
2. Navegue até o diretório do projeto
3. Execute o seguinte comando no terminal:

```bash
docker build -t calculadora-ip .
```

Após isso, execute:

```bash
docker run -p 8080:8080 calculadora-ip
```

A aplicação estará disponível em `http://localhost:8080`

## Licença

Este projeto é open source e está disponível sob a Licença MIT.
# IPcalc-ADS
