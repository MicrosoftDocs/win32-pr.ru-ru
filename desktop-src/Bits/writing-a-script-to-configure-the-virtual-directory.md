---
title: Написание сценария для настройки виртуального каталога
description: Написание сценария для настройки виртуального каталога
ms.assetid: 0324fbc8-1d64-454c-b021-4e010edcac8d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae23a33c2c91dc0a141c6f377daf89708499aae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986173"
---
# <a name="writing-a-script-to-configure-the-virtual-directory"></a><span data-ttu-id="d7c3f-103">Написание сценария для настройки виртуального каталога</span><span class="sxs-lookup"><span data-stu-id="d7c3f-103">Writing a Script to Configure the Virtual Directory</span></span>

<span data-ttu-id="d7c3f-104">Для передачи файла на сервер можно использовать значения свойства IIS BITS по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d7c3f-104">You can use the default BITS IIS property values to upload a file to the server.</span></span> <span data-ttu-id="d7c3f-105">Файл отправки записывается в URL-адрес, указанный в имени удаленного файла задания.</span><span class="sxs-lookup"><span data-stu-id="d7c3f-105">The upload file is written to the URL as specified in the remote file name of the job.</span></span> <span data-ttu-id="d7c3f-106">Чтобы передать файл в серверное приложение и получить ответ, измените свойство [битссервернотификатионтипе](bits-iis-extension-properties.md) для отправки данных по ссылке (отправляет имя файла, содержащего данные) или по значению (отправляет данные в тексте запроса).</span><span class="sxs-lookup"><span data-stu-id="d7c3f-106">To upload the file to a server application and receive a reply, change the [BITSServerNotificationType](bits-iis-extension-properties.md) property to send the data by reference (sends the name of the file that contains the data) or by value (sends the data in the body of the request).</span></span>

<span data-ttu-id="d7c3f-107">Список и описание свойств, которые можно изменить, см. в разделе [Свойства расширения IIS BITS](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d7c3f-107">For a list and description of the properties that you can modify, see [BITS IIS Extension Properties](bits-iis-extension-properties.md).</span></span> <span data-ttu-id="d7c3f-108">Используйте методы интерфейса [**ибитсекстенсионсетуп**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) , чтобы включить и отключить виртуальный каталог для отправки.</span><span class="sxs-lookup"><span data-stu-id="d7c3f-108">Use the methods of the [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) interface to enable and disable the virtual directory for uploads.</span></span>

<span data-ttu-id="d7c3f-109">В следующем примере показано, как использовать сервер сценариев Windows для создания, настройки и включения виртуального каталога IIS для отправки BITS.</span><span class="sxs-lookup"><span data-stu-id="d7c3f-109">The following example shows how to use Windows Script Host to create, configure, and enable an IIS virtual directory for BITS uploads.</span></span>


```JScript
if (WScript.Arguments.length < 2)
{
    WScript.Echo("Usage: bitsvdir virtual_directory local_directory");
    WScript.Quit(1);
}

VirtualDirectoryName = WScript.Arguments(0);
LocalDirectoryName = WScript.Arguments(1);

ServerObj = GetObject("IIS://LocalHost/W3SVC/1/ROOT");
VirtualDir = ServerObj.Create("IIsWebVirtualDir", VirtualDirectoryName );

VirtualDir.Path = LocalDirectoryName;
VirtualDir.AppIsolated = 0;
VirtualDir.AccessScript = true;
VirtualDir.AccessRead = false;
VirtualDir.AccessWrite = false;
VirtualDir.SetInfo();

//Set BITS specific IIS configuration settings
VirtualDir.EnableBITSUploads();
VirtualDir.BITSMaximumUploadSize = "4294967296";
VirtualDir.SetInfo();

WScript.Echo( "Created virtual directory " + VirtualDirectoryName + 
              " with a local directory of " + LocalDirectoryName );
WScript.Quit( 0 );
```



<span data-ttu-id="d7c3f-110">Чтобы изменить предыдущий пример для передачи данных в серверное приложение, добавьте следующий код перед **сетинфо**.</span><span class="sxs-lookup"><span data-stu-id="d7c3f-110">To change the previous example to upload the data to a server application, add the following code before **SetInfo**.</span></span>


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



<span data-ttu-id="d7c3f-111">Расположение файла отправки передается в серверное приложение мясп. ASP в заголовке BITS-Request-File-Name.</span><span class="sxs-lookup"><span data-stu-id="d7c3f-111">The location of the upload file is passed to the server application, myasp.asp, in the BITS-Request-DataFile-Name header.</span></span> <span data-ttu-id="d7c3f-112">Чтобы получить файл отправки в тексте запроса, присвойте свойству [битссервернотификатионтипе](bits-iis-extension-properties.md) значение 2.</span><span class="sxs-lookup"><span data-stu-id="d7c3f-112">To receive the upload file in the body of the request, set the [BITSServerNotificationType](bits-iis-extension-properties.md) property to 2.</span></span>

<span data-ttu-id="d7c3f-113">Сведения о получении данных об отправке в серверное приложение см. в разделе [Использование заголовков запросов и ответов BITS](using-bits-notification-request-response-headers.md).</span><span class="sxs-lookup"><span data-stu-id="d7c3f-113">For information on receiving the upload data in your server application, see [Using BITS Notification Request/Response Headers](using-bits-notification-request-response-headers.md).</span></span>

 

 




