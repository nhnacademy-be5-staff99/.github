# Store99
by Staff 99
nhnacademy

<br>

# Members


# Project Architecture
![image](https://github.com/nhnacademy-be5-staff99/.github/assets/19241369/4cce8cdb-b0ce-4b50-8575-285b1390f7be)
| 리포지토리 | Public IP (플로팅 IP) | Private IP (사설 IP) | PORT (포트) | 인스턴스 이름 | CI/CD 환경 | Login User 이름 | 서버 접속 명령어 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| store99-front | 180.210.83.229 | 192.168.0.65 | 8080 | store99-front | Github Action | store99 | ssh -i github_rsa mailto:store99@180.210.83.229 |
| store99-gateway | 125.6.38.50 | 192.168.0.93 | 8080 | store99-gateway | Github Action | store99 | ssh -i github_rsa mailto:store99@125.6.38.50 |
| store99-auth | 125.6.38.50 | 192.168.0.93 | 8081 | store99-gateway | Github Action | store99 | ssh -i github_rsa mailto:store99@125.6.38.50 |
| store99-eureka | 125.6.38.50 | 192.168.0.93 | 8082 | store99-gateway | Github Action | store99 | ssh -i github_rsa mailto:store99@125.6.38.50 |
| store99-bookstore | 133.186.159.71 | 192.168.0.96 | 8080 | store99-bookstore | Jenkins | store99 | ssh -i github_rsa mailto:store99@133.186.159.71 |
| store99-coupon | 180.210.83.81 | 192.168.0.32 | 8080 | store99-coupon | Jenkins | store99 | ssh -i github_rsa mailto:store99@133.186.159.71180.210.83.81 |
| store99-batch | 133.186.212.35 | 192.168.0.130 | 8080 | store99-batch | Jenkins | store99 | ssh -i github_rsa mailto:store99@133.186.159.71133.186.212.35 |
| store99-elk |  |  |  | store99-elk | Jenkins | store99 |  |

# Pull Reqeust Reviewer
![image](https://github.com/nhnacademy-be5-staff99/.github/assets/19241369/2e6b79f8-9580-4bac-8dae-db2068a78495)
- 동영, 서연 -> 승규 -> 진규, 아현
- 서연, 승규 -> 진규 -> 아현, 현철
- 승규, 진규 -> 아현 -> 현철, 효겸
- 진규, 아현 -> 현철 -> 효겸, 동영
- 아현, 현철 -> 효겸 -> 동영, 서연
- 현쳘, 효겸 -> 동영 -> 서연, 승규
- 효겸, 동영 -> 서연 -> 승규, 진규
