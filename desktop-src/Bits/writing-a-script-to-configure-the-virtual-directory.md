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
ms.openlocfilehash: b9ea1de5a0b9f7be9598a4011cbb6cd76f49e6d4bcc3d468093be1479ee2b59e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004604"
---
# <a name="writing-a-script-to-configure-the-virtual-directory"></a>Написание сценария для настройки виртуального каталога

Для передачи файла на сервер можно использовать значения свойства IIS BITS по умолчанию. Файл отправки записывается в URL-адрес, указанный в имени удаленного файла задания. Чтобы передать файл в серверное приложение и получить ответ, измените свойство [битссервернотификатионтипе](bits-iis-extension-properties.md) для отправки данных по ссылке (отправляет имя файла, содержащего данные) или по значению (отправляет данные в тексте запроса).

Список и описание свойств, которые можно изменить, см. в разделе [Свойства расширения IIS BITS](bits-iis-extension-properties.md). Используйте методы интерфейса [**ибитсекстенсионсетуп**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) , чтобы включить и отключить виртуальный каталог для отправки.

в следующем примере показано, как использовать сервер сценариев Windows для создания, настройки и включения виртуального каталога IIS для отправки BITS.


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



Чтобы изменить предыдущий пример для передачи данных в серверное приложение, добавьте следующий код перед **сетинфо**.


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



Расположение файла отправки передается в серверное приложение мясп. ASP в заголовке BITS-Request-File-Name. Чтобы получить файл отправки в тексте запроса, присвойте свойству [битссервернотификатионтипе](bits-iis-extension-properties.md) значение 2.

Сведения о получении данных об отправке в серверное приложение см. в разделе [Использование заголовков запросов и ответов BITS](using-bits-notification-request-response-headers.md).

 

 




