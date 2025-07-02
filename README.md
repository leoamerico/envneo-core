# EnvNeo · Core Business Logic (CBL)

Este repositório contém o **Modelo de Domínio Unificado (UDM)** da arquitetura EnvNeo.

## Estrutura
core/
├── model/ # Entidades puras (Device, Alert, UserProfile)
├── logic/ # Casos de uso (GenerateAlert, AssignDevice)
└── ports/ # Interfaces para gateways e repositórios

## 🎯 Objetivo

Representar **toda a lógica de negócio** do projeto sem dependências de frameworks ou infraestrutura.

- ❌ Sem Spring, Flutter, Zephyr
- ✅ Apenas Python puro (ou Java/Kotlin, conforme escolha)
- ✅ 100% testável com mocks

## 📦 Exemplo de entidade
```python
class Device:
    def __init__(self, id: str, battery: float):
        self.id = id
        self.battery = battery
        
—

### ✅ `.gitignore`
```gitignore
# Arquivos Python temporários
__pycache__/
*.py[cod]
*.egg-info/
dist/
build/

# IDEs
.vscode/
.idea/

# Arquivos do sistema
.DS_Store
.env
*.log  
