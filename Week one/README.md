# HTTP examples

This reading explores the contents of HTTP requests and responses in more depth.

## **Request Line**

Every HTTP request begins with the request line.

This consists of the HTTP method, the requested resource and the HTTP protocol version.

<code>GET /home.html HTTP/1.1</code>

In this example, <code>GET</code> is the HTTP method, <code>/home.html</code> is the resource requested and HTTP 1.1 is the protocol used.

## **HTTP Methods**

HTTP methods indicate the action that the client wishes to perform on the web server resource.

Common HTTP methods are:

----------------------------------------------------------------------------
| HTTP Method   | Description                                              |
|--------------------------------------------------------------------------|
| GET           | The client requests a resource on the web server         |
| POST          | The client submits data to a resource on the web server  |
| PUT           | The client replaces a resource on the web server         |
| DELETE        | The client deletes a resource on the web server          |
----------------------------------------------------------------------------

## **HTTP Request Headers**

After the request line, the HTTP headers are followed by a line break.

There are various possibilities when including an HTTP header in the HTTP request. A header is a case-insensitive name followed by a: and then followed by a value.

Common headers are:

````
Host: example.com
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.9; rv:50.0) Gecko/20100101 Firefox/50.0
Accept: */*
Accept-Language: en
Content-type: text/json
````

- The <code>Host</code> header specifies the host of the server and indicates where the resource is requested from.

- The <code>User-Agent</code> header informs the web server of the application that is making the request. It often includes the operating system (Windows, Mac, Linux), version and application vendor.

- The <code>Accept</code> header informs the web server what type of content the client will accept as the response.

- The <code>Accept-Language</code> header indicates the language and optionally the locale that the client prefers.

- The <code>Content-type</code> header indicates the type of content being transmitted in the request body.

## **HTTP Request Body**

HTTP requests can optionally include a request body. A request body is often included when using the HTTP POST and PUT methods to transmit data.

````
POST /users HTTP/1.1
Host: example.com

{
 "key1":"value1",
 "key2":"value2",
 "array1":["value3","value4"]
}
````

````
PUT /users/1 HTTP/1.1
Host: example.com
Content-type: text/json

{"key1":"value1"}
````

## **HTTP Responses**

When the web server is finished processing the HTTP request, it will send back an HTTP response.

The first line of the response is the status line. This line shows the client if the request was successful or if an error occurred.

<code>HTTP/1.1 200 OK</code>

The line begins with the HTTP protocol version, followed by the status code and a reason phrase. The reason phrase is a textual representation of the status code.

## **HTTP Status Codes**

The first digit of an HTTP status code indicates the category of the response: Information, Successful, Redirection, Client Error or Server Error.

The common status codes you'll encounter for each category are:

_1XX Informational_

-----------------------------------------------------------------------------------------------------------------------------------
| Status Code |    Reason Phrase     |                                      Description                                           |
|---------------------------------------------------------------------------------------------------------------------------------|
|     100     |      Continue        | The server received the request headers and should continue to send the request body.      |
|     100     |  Switching Protocols | The client has requested the server to switch protocols and the server has agreed to do so |
-----------------------------------------------------------------------------------------------------------------------------------

_2XX Successful_

-----------------------------------------------------------------------------------------------------------------------------------
| Status Code |  Reason Phrase  |                                      Description                                                |
|---------------------------------------------------------------------------------------------------------------------------------|
|     200     |       ok        | Standard response returned by the server to indicate it successfully processed the request.     |
|     201     |   Created       | The server successfully processed the request and a resource was created.                       |
|     202     |   Accepted      | The server accepted the request for processing but the processing has not yet been completed.   |
|     204     |   No Content    | The server successfully processed the request but is not returning any content.                 |
-----------------------------------------------------------------------------------------------------------------------------------

_3XX Redirection_

----------------------------------------------------------------------------------------------------------------------
| Status Code |    Reason Phrase     |                                      Description                              |
|--------------------------------------------------------------------------------------------------------------------|
|     301     |  Moved Permanently   | This request and all future requests should be sent to the returned location. |
|     302     |  Found               | This request should be sent to the returned location.                         |
----------------------------------------------------------------------------------------------------------------------

_4XX Client Error_

--------------------------------------------------------------------------------------------------------------------------------------------------------------
| Status Code |  Reason Phrase  |                                      Description                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     400     |   Bad Request      | The server cannot process the request due to a client error, e.g., invalid request or transmitted data is too large.    |
|     401     |    Unauthorized    | The client making the request is unauthorized and should authenticate.                                                  |
|     403     |     Forbidden      | The request was valid but the server is refusing to process it. This is usually returned due to the client having 
insufficient permissions for the website, e.g., requesting an administrator action but the user is not an administrator.                                     |
|     404     |     Not Found      | The server did not find the requested resource.                                                                         |
|     405     | Method Not Allowed | The web server does not support the HTTP method used.                                                                   |
--------------------------------------------------------------------------------------------------------------------------------------------------------------


_5XX Server Error_

------------------------------------------------------------------------------------------------------------------------------------------------------------
| Status Code |  Reason Phrase  |                                      Description                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|     500     |  Internal Server Error | A generic error status code given when an unexpected error or condition occurred while processing the request.    |
|     502     |  Bad Gateway           | The web server received an invalid response from the Application Server.                                          |
|     503     |  Service Unavailable   | The web server cannot process the request.                                                                        |
------------------------------------------------------------------------------------------------------------------------------------------------------------


## **HTTP Response Headers**

Following the status line, there are optional HTTP response headers followed by a line break.

Similar to the request headers, there are many possible HTTP headers that can be included in the HTTP response.

Common response headers are:

````
Date: Fri, 11 Feb 2022 15:00:00 GMT+2
Server: Apache/2.2.14 (Linux)
Content-Length: 84
Content-Type: text/html
````

- The <code>Date</code> header specifies the date and time the HTTP response was generated.

- The <code>Server</code> header describes the web server software used to generate the response.

- The <code>Content-Length</code> header describes the length of the response.

- The <code>Content-Type</code> header describes the media type of the resource returned (e.g. HTML document, image, video).

## **HTTP Response Body**

Following the HTTP response headers is the HTTP response body. This is the main content of the HTTP response.

This can contain images, video, HTML documents and other media types.

````
HTTP/1.1 200 OK
Date: Fri, 11 Feb 2022 15:00:00 GMT+2
Server: Apache/2.2.14 (Linux)
Content-Length: 84
Content-Type: text/html

<html>
  <head><title>Test</title></head>
  <body>Test HTML page.</body>
</html>
````

# Outros Protocolos de Internet

Os Protocolos de Transferência de Hipertexto (HTTP) são usados sobre o TCP (Transmission Control Protocol) para transferir páginas da Web e outros conteúdos de sites.
Esta leitura explora outros protocolos comumente utilizados na Internet.

## Protocolo DHCP (Dynamic Host Configuration Protocol)

Você aprendeu que os computadores precisam de endereços IP para se comunicarem uns com os outros. Quando o computador se conecta a uma rede, o Protocolo de Configuração Dinâmica de Host ou DHCP, como é comumente conhecido, é usado para atribuir um endereço IP ao computador.
Seu computador se comunica através do protocolo UDP (User Datagram Protocol) usando o protocolo com um tipo de servidor chamado servidor DHCP. O servidor controla os computadores na rede e seus endereços IP. Ele atribuirá ao seu computador um endereço IP e responderá sobre o protocolo para que ele saiba qual endereço IP usar. Depois que o computador tiver um endereço IP, ele poderá se comunicar com outros computadores na rede.

## Protocolo DNS (Sistema de Nomes de Domínio)

Seu computador precisa de uma maneira de saber com qual endereço IP se comunicar quando você visita um site em seu navegador da web, por exemplo, meta.com. O Protocolo do Sistema de Nomes de Domínio, comumente conhecido como DNS, fornece essa função. Em seguida, o computador verifica com o servidor DNS associado ao nome de domínio e, em seguida, retorna o endereço IP correto.

## Protocolo IMAP (Internet Message Access Protocol)

Você verifica seus e-mails em seu dispositivo móvel ou tablet? Ou talvez você use um aplicativo de e-mail em seu computador?
Seu dispositivo precisa de uma maneira de baixar e-mails e gerenciar sua caixa de correio no servidor que armazena seus e-mails. Essa é a finalidade do Internet Message Access Protocol ou IMAP.

## Protocolo SMTP (Simple Mail Transfer Protocol)

Agora que seus e-mails estão em seu dispositivo, você precisa de uma maneira de enviar e-mails. O protocolo SMTP (Simple Mail Transfer Protocol) é usado. Ele permite que os clientes de e-mail enviem e-mails para envio através de um servidor SMTP. Você também pode usá-lo para receber e-mails de um cliente de e-mail, mas o IMAP é mais comumente usado.

## Protocolo dos Correios (POP)

O Post Office Protocol (POP) é um protocolo mais antigo usado para baixar e-mails para um cliente de e-mail. A principal diferença no uso de POP em vez de IMAP é que o POP excluirá os e-mails no servidor depois que eles forem baixados para o seu dispositivo local. Embora não seja mais comumente usado em clientes de e-mail, os desenvolvedores costumam usá-lo para implementar a automação de e-mail, pois é um protocolo mais simples do que o IMAP.

## Protocolo FTP (File Transfer Protocol)

Ao executar seus sites e aplicativos Web na Internet, você precisará de uma maneira de transferir os arquivos do computador local para o servidor em que eles serão executados. O protocolo padrão usado para isso é o File Transfer Protocol ou FTP. FTP permite listar, enviar, receber e excluir arquivos em um servidor. Seu servidor deve executar um servidor FTP e você precisará de um cliente FTP em sua máquina local. Você aprenderá mais sobre eles em um curso posterior.

## Protocolo SSH (Secure Shell Protocol)

Quando você começar a trabalhar com servidores, também precisará de uma maneira de fazer login e interagir com o computador remotamente. O método mais comum de fazer isso é usando o protocolo Secure Shell, comumente conhecido como SSH. O uso de um cliente SSH permite que você se conecte a um servidor SSH em execução em um servidor para executar comandos no computador remoto.
Todos os dados enviados por SSH são criptografados. Isso significa que terceiros não podem entender os dados transmitidos. Somente os computadores de envio e recebimento podem entender os dados.

## Protocolo de transferência de arquivos SSH (SFTP)

Os dados são transmitidos de forma insegura ao usar o Protocolo de Transferência de Arquivos. Isso significa que terceiros podem entender os dados que você está enviando. Isso não é certo se você transmitir arquivos da empresa, como software e bancos de dados. Para resolver isso, o SSH File Transfer Protocol, alternativamente chamado de Secure File Transfer Protocol, pode ser usado para transferir arquivos através do protocolo SSH. Isso garante que os dados sejam transmitidos com segurança. A maioria dos clientes FTP também suporta o protocolo SFTP.
