---
title: Использование заголовков запросов и ответов BITS
description: BITS может отправить расположение файла отправки (по ссылке) в серверное приложение или отправить файл отправки в тексте запроса (по значению).
ms.assetid: b80f9077-54e7-4d10-909a-dee7d8822627
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 5dcbee8b82d96a4f13db0ae4de6441e9df40ce83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252811"
---
# <a name="using-bits-notification-requestresponse-headers"></a>Использование заголовков запросов и ответов BITS

BITS может отправить расположение файла отправки (по ссылке) в серверное приложение или отправить файл отправки в тексте запроса (по значению). Чтобы указать, как служба BITS отправляет файл отправки в серверное приложение, установите свойство метабазы IIS [**битссервернотификатионтипе**](bits-iis-extension-properties.md). Если указать по ссылке, BITS передает расположение файла в заголовке BITS-Request-File-Name. Чтобы отправить ответ, создайте и запишите ответ на файл, указанный в заголовке BITS-Response-File-Name.

Серверные приложения, которые отправляют один и тот же ответ нескольким клиентам, должны использовать по ссылке, поэтому на сервере существует только одна копия ответа. Например, в приложении обновления программного обеспечения клиент загружает конфигурацию программного обеспечения в серверное приложение. Серверное приложение определяет, какой пакет требуется клиенту, и отправляет URL-адрес пакета в службу BITS. Затем служба BITS скачивает пакет в качестве ответа.

Серверные приложения, генерирующие уникальные ответы для каждого клиента, должны использовать по значению. Например, серверное приложение, которое поддерживает приобретение музыкальных файлов, должно отправить подписанный музыкальный файл клиенту. Так как подписанный музыкальный файл уникален для клиента, серверное приложение не будет хранить его на сервере. По значению также полезно для приложения, которое уже написано для приема данных веб-клиента напрямую.

Дополнительные сведения о заголовках запросов и ответов, используемых между BITS и серверным приложением, см. в разделе [протокол уведомлений для серверных приложений](notification-protocol-for-server-applications.md).

В следующем примере JavaScript показано, как получить доступ к файлам запросов и ответов в серверном приложении, использующем уведомление по ссылке (BITS передает расположение файлов в заголовках).


```JavaScript
  var fso = new ActiveXObject ("Scripting.FileSystemObject")
  var requestFileName = Request.ServerVariables ("HTTP_BITS-Request-DataFile-Name")
  var responseFileName = Request.ServerVariables ("HTTP_BITS-Response-DataFile-Name")
  var requestStream
  var responseStream
  var ForReading = 1
  var ForWriting = 2
  var TristateUseDefault = -2

  //Open the upload data file as text stream for reading.
  requestStream = fso.OpenTextFile(requestFileName, ForReading, false, TristateUseDefault);

  //Do something with the uploaded data.

  //Close the upload stream.
  requestStream.Close()

  //Open response data file as text stream for writing.
  responseStream = fso.OpenTextFile(responseFileName, ForWriting, true, TristateUseDefault);

  //Write a response to the response file.

  //Close the response text stream
  responseStream.Close()
```



Если вы хотите использовать файл ответов, отличный от того, который указан в параметре BITS-Response-File-Name, вызовите метод **Response. аддхеадер** , чтобы добавить URL-адрес, как показано в следующем примере. Если указан другой файл ответов, не создавайте файл ответов, указанный в файле BITS-Response-File-Name.


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




