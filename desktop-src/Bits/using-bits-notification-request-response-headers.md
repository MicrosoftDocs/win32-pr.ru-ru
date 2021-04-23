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
# <a name="using-bits-notification-requestresponse-headers"></a><span data-ttu-id="ee0f3-103">Использование заголовков запросов и ответов BITS</span><span class="sxs-lookup"><span data-stu-id="ee0f3-103">Using BITS Notification Request/Response Headers</span></span>

<span data-ttu-id="ee0f3-104">BITS может отправить расположение файла отправки (по ссылке) в серверное приложение или отправить файл отправки в тексте запроса (по значению).</span><span class="sxs-lookup"><span data-stu-id="ee0f3-104">BITS can send the location of the upload file (by reference) to your server application or it can send the upload file in the body of the request (by value).</span></span> <span data-ttu-id="ee0f3-105">Чтобы указать, как служба BITS отправляет файл отправки в серверное приложение, установите свойство метабазы IIS [**битссервернотификатионтипе**](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ee0f3-105">To specify how BITS sends the upload file to your server application, set the IIS metabase property, [**BITSServerNotificationType**](bits-iis-extension-properties.md).</span></span> <span data-ttu-id="ee0f3-106">Если указать по ссылке, BITS передает расположение файла в заголовке BITS-Request-File-Name.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-106">If you specify by reference, BITS passes the location of the file in the BITS-Request-DataFile-Name header.</span></span> <span data-ttu-id="ee0f3-107">Чтобы отправить ответ, создайте и запишите ответ на файл, указанный в заголовке BITS-Response-File-Name.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-107">To send a reply, create and write your response to the file specified in the BITS-Response-DataFile-Name header.</span></span>

<span data-ttu-id="ee0f3-108">Серверные приложения, которые отправляют один и тот же ответ нескольким клиентам, должны использовать по ссылке, поэтому на сервере существует только одна копия ответа.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-108">Server applications that send the same reply to many clients should use by reference, so there is only one copy of the reply on the server.</span></span> <span data-ttu-id="ee0f3-109">Например, в приложении обновления программного обеспечения клиент загружает конфигурацию программного обеспечения в серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-109">For example, in a software update application, the client would upload its software configuration to the server application.</span></span> <span data-ttu-id="ee0f3-110">Серверное приложение определяет, какой пакет требуется клиенту, и отправляет URL-адрес пакета в службу BITS.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-110">The server application determines which package the client needs and sends the URL of the package to BITS.</span></span> <span data-ttu-id="ee0f3-111">Затем служба BITS скачивает пакет в качестве ответа.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-111">Then, BITS downloads the package as the reply.</span></span>

<span data-ttu-id="ee0f3-112">Серверные приложения, генерирующие уникальные ответы для каждого клиента, должны использовать по значению.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-112">Server applications that generate unique replies for each client should use by value.</span></span> <span data-ttu-id="ee0f3-113">Например, серверное приложение, которое поддерживает приобретение музыкальных файлов, должно отправить подписанный музыкальный файл клиенту.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-113">For example, a server application that supports the purchase of music files would need to send a signed music file to the client.</span></span> <span data-ttu-id="ee0f3-114">Так как подписанный музыкальный файл уникален для клиента, серверное приложение не будет хранить его на сервере.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-114">Because the signed music file is unique to the client, the server application would not store it on the server.</span></span> <span data-ttu-id="ee0f3-115">По значению также полезно для приложения, которое уже написано для приема данных веб-клиента напрямую.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-115">By value is also useful for an application that is already written to accept web client data directly.</span></span>

<span data-ttu-id="ee0f3-116">Дополнительные сведения о заголовках запросов и ответов, используемых между BITS и серверным приложением, см. в разделе [протокол уведомлений для серверных приложений](notification-protocol-for-server-applications.md).</span><span class="sxs-lookup"><span data-stu-id="ee0f3-116">For details on the request and response headers used between BITS and your server application, see [Notification Protocol for Server Applications](notification-protocol-for-server-applications.md).</span></span>

<span data-ttu-id="ee0f3-117">В следующем примере JavaScript показано, как получить доступ к файлам запросов и ответов в серверном приложении, использующем уведомление по ссылке (BITS передает расположение файлов в заголовках).</span><span class="sxs-lookup"><span data-stu-id="ee0f3-117">The following JavaScript example shows how to access the request and response files in a server application that uses by reference notification (BITS passes the location of the files in the headers).</span></span>


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



<span data-ttu-id="ee0f3-118">Если вы хотите использовать файл ответов, отличный от того, который указан в параметре BITS-Response-File-Name, вызовите метод **Response. аддхеадер** , чтобы добавить URL-адрес, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-118">If you want to use a different response file than the one specified in BITS-Response-DataFile-Name, call the **Response.AddHeader** method to add the BITS-Static-Response-URL as shown in the following example.</span></span> <span data-ttu-id="ee0f3-119">Если указан другой файл ответов, не создавайте файл ответов, указанный в файле BITS-Response-File-Name.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-119">If you specify a different response file, do not create the response file specified in BITS-Response-DataFile-Name.</span></span>


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




