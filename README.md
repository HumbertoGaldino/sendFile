# sendFile
Uso do método sendFile() de um servidor HTTP com Routing &amp; Response utilizando Express, aplicado no curso Web Fullstack da Digital House.

>O método sendFile() faz parte do objeto de resposta do Express. E nos permite o envio de arquivos do servidor de forma fácil ao cliente em resposta as requisições do cliente.

>Primeiro precisamos do módulo de path, que vem nativamente, para que se possa gerar a rota. Dentro do path utilizamos o join(), que nos fornece o caminho do arquivo. Ele será o responsável por juntar as peças do percurso, tendo em conta o sistema operacional em que nos encontramos(Mac, Windows ou Linux).

```
    const path = require('path');

    app.get('/', (req,res)=>{
        res.sendFile(path.join(__dirname,'/views/index.html));
    });
```

>*__dirname* é uma constante Node.js que se refere ao diretório do que arquivo que está sendo executado. */views/index.html* é o caminho relativo ao arquivo que queremos enviar.

