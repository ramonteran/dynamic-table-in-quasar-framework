# Dynamic-table-in-quasar-framework
dynamic table in quasar framework with add, update and delete. focused on component reuse...

<h1>El primer paso es crear el archivo docker-compose.yml en el proyecto para garantizar el despliegue en cualquiera máquina usando Docker…</h1> 
<section>
    <div class="row">

            version: '1'

            services:
            dynamic-table-in-quasar-framework:
                image: ramonteran/quasar-cli:1.0
                container_name: Dynamic-table-in-quasar-framework
                working_dir: /home/node/app/admin
                command: /bin/sh -c "yarn && quasar dev"
                ports: 
                - "9100:9100"
                volumes: 
                - ./dynamic-table-in-quasar-framework:/home/node/app/admin
                restart: always
                stdin_open: true
                tty: true
                environment:
                - CHOKIDAR_USEPOLLING=true
    </div>
</section>