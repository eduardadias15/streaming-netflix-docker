# Plataforma de Streaming Self-Hosted com Docker

Projeto prático desenvolvido na disciplina de Computação em Nuvem 
— Ciência da Computação — UNICEPLAC.

## Sobre o Projeto
Implementação de uma plataforma de streaming self-hosted inspirada 
na Netflix, utilizando apenas ferramentas gratuitas e de código aberto.
O ambiente foi configurado em uma Máquina Virtual com Debian 12.

## Ambiente
- **Virtualização:** Máquina Virtual (VM)
- **Sistema Operacional:** Debian 12 Bookworm

## Tecnologias Utilizadas
| Ferramenta | Versão | Função |
|---|---|---|
| Docker Engine | 29.5.3 | Motor de execução de containers |
| Docker Compose | v5.1.4 | Orquestração dos serviços |
| Jellyfin | 10.11.11 | Interface de streaming estilo Netflix |
| Portainer CE | 2.x | Gerenciamento visual dos containers |
| Nginx Proxy Manager | latest | Proxy reverso e acesso web |

## Estrutura do Projeto
netflix-free/
 -docker-compose.yml
 -jellyfin/config/   → Configurações do Jellyfin
 -jellyfin/cache/    → Cache de transcodificação
 -portainer/data/    → Dados do Portainer
 -nginx/data/        → Configurações do Nginx
 -data/media/
 -movies/            → 10 filmes
 -series/            → 3 séries / 7 episódios

## Como Executar
```bash
docker compose up -d
docker ps
```

## Prints do Projeto
![Docker PS]
![Jellyfin]
![Portainer]
![Nginx]

## Dificuldades Encontradas
- Permissão negada ao Docker Socket (resolvido com usermod)
- Timeout do Portainer no primeiro acesso
- Instabilidade da VM durante uso do Vim

## Melhorias Futuras
- HTTPS com Let's Encrypt
- Monitoramento com Grafana + Prometheus
- Migração para VPS em nuvem

## Autor
**Eduarda Dias**  
Curso: Ciência da computação — UNICEPLAC  
[www.linkedin.com/in/eduarda-dias-693711393]
