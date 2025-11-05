# DNS in Detail — Notas da sessão

**Resumo:**
Aprendi o básico sobre DNS, os tipos de registro e como usar `nslookup` para consultar esses registros.

## O que é DNS

* **DNS (Domain Name System):** converte nomes de domínio (ex.: `exemplo.com`) em endereços/recursos (IPs, mail servers, etc).

## Record types que vi

* **A** — endereço IPv4
* **AAAA** — endereço IPv6
* **CNAME** — alias para outro nome
* **MX** — servidores de e‑mail (com prioridade)
* **TXT** — textos usados para SPF/DKIM/validação
* **NS** — servidores de nome autoritativos

## Comandos `nslookup` (consultas por tipo)

```
# consulta padrão (A)
nslookup exemplo.com

# consultar A explicitamente
nslookup -type=a exemplo.com

# consultar AAAA
nslookup -type=aaaa exemplo.com

# consultar CNAME
nslookup -type=cname subdominio.exemplo.com

# consultar MX
nslookup -type=mx exemplo.com

# consultar TXT
nslookup -type=txt exemplo.com

# consultar NS (servidores autoritativos)
nslookup -type=ns exemplo.com

# usar um servidor DNS específico (ex.: Google DNS)
nslookup exemplo.com 8.8.8.8
```

## Arquivos no repositório

* `notes.md` (este arquivo)
* `completed.png` (print da conclusão)
