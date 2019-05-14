
haproxy with keepalived

admin url:
    http://0.0.0.0:9000/admin?stats
    admin/admin

http_8080_frontend:
    http://0.0.0.0:8080
    http://0.0.0.0:8080/admin/stats

https_8443_frontend
    http://0.0.0.0:8443
    http://0.0.0.0:8443/admin/stats

http_8080_backend
    server          backend-192.168.8.236:8080 192.168.8.236:8080 check inter 1000
    server          backend-192.168.8.237:8080 192.168.8.237:8080 check inter 1000
