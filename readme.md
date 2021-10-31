* Estudos no curso Alura HTTP
O HTTP é definir regras de conexão
- http
- https ( ssl / tls) Criptografar
Podemos usar essa url para consultar os parametros e cabeçalhos
-https://datatracker.ietf.org/doc/html/rfc2616

-As chaves públicas estão no certificado, a chave privada fica apenas no servidor


* Endereços 127.198.2.90
* DNS ele pega o www.alura.com.br e converte para o endereço
* Usamos a porta 80 no http e porta 443 https

https://www.asilas.com.br:443/cv
https => Protocolo
asilas => Dominio
443 => Recurso
cv => Recurso
=======================================

HTTP => É Stateless ele não guarda requisição, é unico.
Requisição: www.cea.com.br
Resposta: 
2XX Sucesso
3XX Redirect
4XX Client Error
5XX Server Error

=======================================

Métodos:
GET => Solicitar dados
POST => Enviar dados
DELETE => Excluir dados
PUT => Atualizar dados

=======================================

* Serviço REST
Recursos => URI , são definidos via URI

* Operações =>  GET POT PUST DELETE
Representação => Json - XML - HTML
Cabeçalhos => Accept/Content-Type para especificar a representação acima.
MIME types são tipo e subtipos.
Tipo => text, image, application, audio e video
Subtipo => text/plain, text/html, text/css, text/javascript
            image -> image/gif, image/png, image/jpeg
            audio -> audio/midi, audio/mpeg, audio/webm, audio/ogg, audio/wav
            video -> video/mp4
            application -> application/xml,  application/pdf
        

=======================================

HTTP2 na sua versão 2

* Consultar uma uri => 
curl www.asilas.com.br ou curl -v www.asilas.com.br

* Requisição => 
> GET / HTTP/1.1
[ Host: www.caelum.com.br
  User-Agent: curl/7.49.1
  Accept: */* ] 

[] Headers 

* Resposta =>
< HTTP/1.1 200 OK
< Content-Type: text/html; charset=utf-8
< Vary: Accept-Encoding,User-Agent
< Content-Language: pt-br
< Content-Type: text/html;charset=UTF-8
< X-DNS-Prefetch-Control: on
< X-Cloud-Trace-Context: 3e5e270ee3ab1e79f81b10d2cdef53cd
< Date: Fri, 24 Mar 2017 19:20:12 GMT
< Server: Google Frontend
< Content-Length: 95776

* Abaixo o corpo de resposta

 <!DOCTYPE html> <html class="no-js"lang="pt-br"> <head> <title>Caelum | Cursos de Java, .NET, Android, PHP, Scrum, HTML, CSS e JavaScript </title>  <meta name="viewport"content="width=device-width,initial-scale=1"> <meta name="format-detection"content="telephone=no"> <meta name="referrer"content="origin">   <meta name="description"content="A Caelum tem os cursos de Java, Scrum, Web, Front-end, PHP, .NET e Mobile mais reconhecidos no mercado, com didática diferenciada e instrutores qualificados.">    <link rel="canonical"href="https://www.caelum.com.br/">     <style>.calendario .sem-turmas,.calendario-compacto .mais-turmas,.fm-message.fm-warning{font-style:italic}

Observações =>
Enviamos comprimido os dados no modo ( GZIP )
E os texto enviando via ( Binário ) tanto request quando response
Após os enviou binário também ele é comprimido via ( HPACK )
Por fim ele é criptografado pelo ( TLS )


=======================================

* Headers Stateful HTTP2
Ele envia apenas os novos cabeçalhos sem precisar repetir novamente( GUARDA OS DADOS ), caso ele já enviou.
Diferente do http1.0



=======================================










