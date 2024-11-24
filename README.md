Heavily inspired by [docker-compose-nas](https://github.com/AdrienPoupa/docker-compose-nas/tree/master)

Need to have:
- Cloudflare API token with rights to domain
- echo $(htpasswd -nb "user" "pass") | sed -e "s/\\$/\\$\\$/g"
- domain

Steps:
- spin up adguard container with loadbalancer label to port 3000
- add to /etc/hosts the domain route <ip> <adguard.domain>
- set it up
- add adguard device ip as DNS in router
- add DNS rewrites to local domains
- you can clear the /etc/hosts
