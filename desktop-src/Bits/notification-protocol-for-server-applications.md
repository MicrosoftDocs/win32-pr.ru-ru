---
title: Протокол уведомлений для серверных приложений
description: Служба BITS использует свойство Битссервернотификатионтипе, чтобы определить, как BITS отправляет содержимое файла отправки в серверное приложение.
ms.assetid: d5193d0c-3ab4-47ab-a570-fea2904a4371
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d35f6f5fec1a1de9ebd5c2c244a55bc1806b06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986219"
---
# <a name="notification-protocol-for-server-applications"></a><span data-ttu-id="a867c-103">Протокол уведомлений для серверных приложений</span><span class="sxs-lookup"><span data-stu-id="a867c-103">Notification Protocol for Server Applications</span></span>

<span data-ttu-id="a867c-104">Служба BITS использует свойство [битссервернотификатионтипе](bits-iis-extension-properties.md) , чтобы определить, как BITS отправляет содержимое файла отправки в серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="a867c-104">BITS uses the [BITSServerNotificationType](bits-iis-extension-properties.md) property to determine how BITS sends the contents of the upload file to the server application.</span></span> <span data-ttu-id="a867c-105">Если свойство Битссервернотификатионтипе имеет значение 1, [то BITS передает расположение файла отправки в заголовок](#sending-the-location-of-the-upload-file-in-a-header).</span><span class="sxs-lookup"><span data-stu-id="a867c-105">If the BITSServerNotificationType property is set to 1, [BITS passes the location of the upload file in a header](#sending-the-location-of-the-upload-file-in-a-header).</span></span> <span data-ttu-id="a867c-106">Если свойство Битссервернотификатионтипе имеет значение 2, то [BITS передает содержимое файла отправки в тексте запроса](#sending-the-upload-file-in-the-body-of-the-request).</span><span class="sxs-lookup"><span data-stu-id="a867c-106">If the BITSServerNotificationType property is set to 2, [BITS passes the contents of the upload file in the body of the request](#sending-the-upload-file-in-the-body-of-the-request).</span></span>

<span data-ttu-id="a867c-107">Дополнительные сведения о том, как служба BITS обрабатывает ошибки серверного приложения, см. в разделе [Обработка ошибок серверного](#handling-server-application-errors)приложения.</span><span class="sxs-lookup"><span data-stu-id="a867c-107">For details on how BITS handles errors from the server application, see [Handling server application errors](#handling-server-application-errors).</span></span>

## <a name="sending-the-location-of-the-upload-file-in-a-header"></a><span data-ttu-id="a867c-108">Отправка расположения файла отправки в заголовке</span><span class="sxs-lookup"><span data-stu-id="a867c-108">Sending the location of the upload file in a header</span></span>

<span data-ttu-id="a867c-109">BITS передает расположение файлов отправки и ответов в серверное приложение в заголовках, если свойство [битссервернотификатионтипе](bits-iis-extension-properties.md) имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="a867c-109">BITS passes the location of the upload and reply files to the server application in the headers if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1.</span></span> <span data-ttu-id="a867c-110">Серверное приложение открывает файл отправки, обрабатывает данные, а затем создает ответный файл.</span><span class="sxs-lookup"><span data-stu-id="a867c-110">The server application opens the upload file, processes the data, and then generates the reply file.</span></span> <span data-ttu-id="a867c-111">По умолчанию служба BITS удаляет файлы отправки и ответа с сервера после получения ответа от серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="a867c-111">By default, BITS removes the upload and reply files from the server after it receives the response from the server application.</span></span> <span data-ttu-id="a867c-112">Чтобы служба BITS скопировала файл отправки в расположение, указанное именем удаленного файла в задании, включите в ответ заголовок BITS-Copy-File-to-Destination.</span><span class="sxs-lookup"><span data-stu-id="a867c-112">To have BITS copy the upload file to the location specified by the remote file name in the job, include the BITS-Copy-File-To-Destination header in your response.</span></span> <span data-ttu-id="a867c-113">Если вы не включаете заголовок и хотите сохранить файлы для отправки и ответа, необходимо скопировать файлы отправки и ответа в новое расположение перед ответом.</span><span class="sxs-lookup"><span data-stu-id="a867c-113">If you do not include the header and you want to save the upload and reply files, you must copy the upload and reply files to a new location before responding.</span></span> <span data-ttu-id="a867c-114">В следующей таблице показаны заголовки запросов.</span><span class="sxs-lookup"><span data-stu-id="a867c-114">The following table shows the request headers.</span></span>



| <span data-ttu-id="a867c-115">Заголовок запроса</span><span class="sxs-lookup"><span data-stu-id="a867c-115">Request header</span></span>              | <span data-ttu-id="a867c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a867c-116">Description</span></span>                                                                                |
|-----------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a867c-117">BITS-исходный-Request-URL</span><span class="sxs-lookup"><span data-stu-id="a867c-117">BITS-Original-Request-URL</span></span>   | <span data-ttu-id="a867c-118">Содержит удаленное имя, указанное в задании.</span><span class="sxs-lookup"><span data-stu-id="a867c-118">Contains the remote name specified in the job.</span></span>                                             |
| <span data-ttu-id="a867c-119">BITS-Request-файл-имя</span><span class="sxs-lookup"><span data-stu-id="a867c-119">BITS-Request-DataFile-Name</span></span>  | <span data-ttu-id="a867c-120">Содержит полный путь к отправленным данным.</span><span class="sxs-lookup"><span data-stu-id="a867c-120">Contains the full path to the uploaded data.</span></span>                                               |
| <span data-ttu-id="a867c-121">BITS-Response-файл-имя</span><span class="sxs-lookup"><span data-stu-id="a867c-121">BITS-Response-DataFile-Name</span></span> | <span data-ttu-id="a867c-122">Содержит полный путь к папке, в которой служба BITS должна записывать ответ на серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="a867c-122">Contains the full path to where BITS expects the server application to write the response.</span></span> |



 

<span data-ttu-id="a867c-123">В следующей таблице показаны заголовки ответов.</span><span class="sxs-lookup"><span data-stu-id="a867c-123">The following table shows the response headers.</span></span>



| <span data-ttu-id="a867c-124">Заголовок ответа</span><span class="sxs-lookup"><span data-stu-id="a867c-124">Response header</span></span>               | <span data-ttu-id="a867c-125">Описание</span><span class="sxs-lookup"><span data-stu-id="a867c-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a867c-126">BITS-статический-Response-URL</span><span class="sxs-lookup"><span data-stu-id="a867c-126">BITS-Static-Response-URL</span></span>      | <span data-ttu-id="a867c-127">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a867c-127">Optional.</span></span> <span data-ttu-id="a867c-128">Содержит абсолютный URL-адрес (не указывайте относительный URL-адрес) для статического файла данных, который будет использоваться в качестве ответа.</span><span class="sxs-lookup"><span data-stu-id="a867c-128">Contains the absolute URL (do not specify a relative URL) to a static data file to use as the response.</span></span> <span data-ttu-id="a867c-129">Файл статических данных должен быть доступен клиенту BITS.</span><span class="sxs-lookup"><span data-stu-id="a867c-129">The static data file must be accessible by the BITS client.</span></span> <span data-ttu-id="a867c-130">При использовании этого заголовка не создавайте файл ответов, указанный в заголовке запроса BITS-Response-File-Name.</span><span class="sxs-lookup"><span data-stu-id="a867c-130">If you use this header, do not create the response file specified in the BITS-Response-DataFile-Name request header.</span></span> <span data-ttu-id="a867c-131">Обратите внимание, что служба BITS не удаляет этот файл.</span><span class="sxs-lookup"><span data-stu-id="a867c-131">Note that BITS does not delete this file for you.</span></span><br/>                                                                                                           |
| <span data-ttu-id="a867c-132">BITS-Copy-File-to-Destination</span><span class="sxs-lookup"><span data-stu-id="a867c-132">BITS-Copy-File-To-Destination</span></span> | <span data-ttu-id="a867c-133">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a867c-133">Optional.</span></span> <span data-ttu-id="a867c-134">По умолчанию, если свойство [битссервернотификатионтипе](bits-iis-extension-properties.md) имеет значение 1 или 2, сервер BITS не копирует файл отправки в расположение, указанное именем удаленного файла в задании.</span><span class="sxs-lookup"><span data-stu-id="a867c-134">By default, if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1 or 2, the BITS server does not copy the upload file to the location specified by the remote file name in the job.</span></span> <span data-ttu-id="a867c-135">Чтобы служба BITS скопировала файл в расположение, указанное именем удаленного файла в задании, отправьте этот заголовок ответа.</span><span class="sxs-lookup"><span data-stu-id="a867c-135">To have BITS copy the file to the location specified by the remote file name in the job, send this response header.</span></span> <span data-ttu-id="a867c-136">Можно указать любое значение; В БИТАХ не используется значение.</span><span class="sxs-lookup"><span data-stu-id="a867c-136">You can specify any value; BITS does not use the value.</span></span> <span data-ttu-id="a867c-137">Обратите внимание, что папки в пути к удаленному файлу должны существовать.</span><span class="sxs-lookup"><span data-stu-id="a867c-137">Note that the folders in the remote file path must exist.</span></span> |



 

<span data-ttu-id="a867c-138">В следующем запросе показаны биты, отправляющие расположение файла отправки в серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="a867c-138">The following request shows BITS sending the location of the upload file to the server application.</span></span>

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
BITS-Request-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\request
BITS-Response-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\response
Content-Length: 0
```

<span data-ttu-id="a867c-139">Ниже показано, как серверное приложение отвечает на BITS; ответ помещается в файл, указанный в заголовке запроса BITS-Response-File-Name.</span><span class="sxs-lookup"><span data-stu-id="a867c-139">The following shows the server application's reply to BITS; the reply is placed in the file specified by the BITS-Response-DataFile-Name request header.</span></span>

``` syntax
HTTP/1.1 200 - OK
Content-Length: 0
```

## <a name="sending-the-upload-file-in-the-body-of-the-request"></a><span data-ttu-id="a867c-140">Отправка файла отправки в тексте запроса</span><span class="sxs-lookup"><span data-stu-id="a867c-140">Sending the upload file in the body of the request</span></span>

<span data-ttu-id="a867c-141">BITS отправляет файл отправки в тело запроса, если свойство [битссервернотификатионтипе](bits-iis-extension-properties.md) имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="a867c-141">BITS sends the upload file in the body of the request if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 2.</span></span> <span data-ttu-id="a867c-142">Отправка файла отправки в теле запроса позволяет существующим сценариям и приложениям работать с минимальными изменениями.</span><span class="sxs-lookup"><span data-stu-id="a867c-142">Sending the upload file in the body of the request lets existing scripts and applications work with minimal modifications.</span></span> <span data-ttu-id="a867c-143">Файл отправки и ответ передаются в запросе и ответе соответственно.</span><span class="sxs-lookup"><span data-stu-id="a867c-143">The upload file and reply file are passed in the request and response, respectively.</span></span> <span data-ttu-id="a867c-144">В следующей таблице показан заголовок запроса.</span><span class="sxs-lookup"><span data-stu-id="a867c-144">The following table shows the request header.</span></span>



| <span data-ttu-id="a867c-145">Заголовок запроса</span><span class="sxs-lookup"><span data-stu-id="a867c-145">Request header</span></span>            | <span data-ttu-id="a867c-146">Описание</span><span class="sxs-lookup"><span data-stu-id="a867c-146">Description</span></span>                                    |
|---------------------------|------------------------------------------------|
| <span data-ttu-id="a867c-147">BITS-исходный-Request-URL</span><span class="sxs-lookup"><span data-stu-id="a867c-147">BITS-Original-Request-URL</span></span> | <span data-ttu-id="a867c-148">Содержит удаленное имя, указанное в задании.</span><span class="sxs-lookup"><span data-stu-id="a867c-148">Contains the remote name specified in the job.</span></span> |



 

<span data-ttu-id="a867c-149">В следующей таблице показаны заголовки ответов.</span><span class="sxs-lookup"><span data-stu-id="a867c-149">The following table shows the response headers.</span></span>



| <span data-ttu-id="a867c-150">Заголовок ответа</span><span class="sxs-lookup"><span data-stu-id="a867c-150">Response header</span></span>               | <span data-ttu-id="a867c-151">Описание</span><span class="sxs-lookup"><span data-stu-id="a867c-151">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a867c-152">BITS-статический-Response-URL</span><span class="sxs-lookup"><span data-stu-id="a867c-152">BITS-Static-Response-URL</span></span>      | <span data-ttu-id="a867c-153">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a867c-153">Optional.</span></span> <span data-ttu-id="a867c-154">Содержит абсолютный URL-адрес (не указывайте относительный URL-адрес) для статического файла данных, который будет использоваться в качестве ответа.</span><span class="sxs-lookup"><span data-stu-id="a867c-154">Contains the absolute URL (do not specify a relative URL) to a static data file to use as the response.</span></span> <span data-ttu-id="a867c-155">Файл статических данных должен быть доступен клиенту BITS.</span><span class="sxs-lookup"><span data-stu-id="a867c-155">The static data file must be accessible by the BITS client.</span></span> <span data-ttu-id="a867c-156">При использовании этого заголовка не включайте ответ в поток.</span><span class="sxs-lookup"><span data-stu-id="a867c-156">If you use this header, do not include the response in the stream.</span></span> <span data-ttu-id="a867c-157">Обратите внимание, что служба BITS не удаляет этот файл.</span><span class="sxs-lookup"><span data-stu-id="a867c-157">Note that BITS does not delete this file for you.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="a867c-158">BITS-Copy-File-to-Destination</span><span class="sxs-lookup"><span data-stu-id="a867c-158">BITS-Copy-File-To-Destination</span></span> | <span data-ttu-id="a867c-159">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="a867c-159">Optional.</span></span> <span data-ttu-id="a867c-160">Если свойство [битссервернотификатионтипе](bits-iis-extension-properties.md) имеет значение 1 или 2, сервер BITS не копирует файл отправки в расположение, указанное именем удаленного файла в задании.</span><span class="sxs-lookup"><span data-stu-id="a867c-160">If the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1 or 2, the BITS server does not copy the upload file to the location specified by the remote file name in the job.</span></span> <span data-ttu-id="a867c-161">Чтобы служба BITS скопировала файл в расположение, указанное с помощью имени удаленного файла, отправьте этот заголовок ответа.</span><span class="sxs-lookup"><span data-stu-id="a867c-161">To have BITS copy the file to the location specified by the remote file name, send this response header.</span></span> <span data-ttu-id="a867c-162">Можно указать любое значение; В БИТАХ не используется значение.</span><span class="sxs-lookup"><span data-stu-id="a867c-162">You can specify any value; BITS does not use the value.</span></span> <span data-ttu-id="a867c-163">Обратите внимание, что папки в пути к удаленному файлу должны существовать.</span><span class="sxs-lookup"><span data-stu-id="a867c-163">Note that the folders in the remote file path must exist.</span></span> |



 

<span data-ttu-id="a867c-164">В следующем запросе показаны биты передачи отправленного файла в серверное приложение в тексте запроса.</span><span class="sxs-lookup"><span data-stu-id="a867c-164">The following request shows BITS passing the uploaded file to the server application in the body of the request.</span></span>

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
Content-Length: 80000

80000 bytes of upload data goes here
```

<span data-ttu-id="a867c-165">Следующий ответ показывает, что серверное приложение передает ответные данные в биты в тексте ответа.</span><span class="sxs-lookup"><span data-stu-id="a867c-165">The following reply shows the server application passing the reply data to BITS in the body of the response.</span></span>

``` syntax
HTTP/1.1 200 - OK
Content-Length: 100

100 bytes of reply data goes here
```

## <a name="handling-server-application-errors"></a><span data-ttu-id="a867c-166">Обработка ошибок серверного приложения</span><span class="sxs-lookup"><span data-stu-id="a867c-166">Handling server application errors</span></span>

<span data-ttu-id="a867c-167">См. раздел [Обработка ошибок серверного приложения](handling-server-application-errors.md).</span><span class="sxs-lookup"><span data-stu-id="a867c-167">See [Handling Server Application Errors](handling-server-application-errors.md).</span></span>

 

 





