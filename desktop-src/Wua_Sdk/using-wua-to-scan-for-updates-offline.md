---
description: Агент Центр обновления Windows (WUA) можно использовать для проверки компьютеров на наличие обновлений безопасности без подключения к Центр обновления Windows или серверу Windows Server Update Services (WSUS), что позволяет проверять наличие обновлений безопасности на компьютерах, которые не подключены к Интернету. Для автономного сканирования на наличие обновлений требуется скачивание подписанного файла Wsusscn2.cab из Центр обновления Windows.
ms.assetid: 452b53af-0f7b-435e-bf12-dd9d84cbd564
title: Использование агента WUA для проверки наличия обновлений в автономном режиме
ms.topic: article
ms.date: 07/23/2020
ms.openlocfilehash: 242ff3655f4ab469d8d768a94f8dc8e529e0da74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342722"
---
# <a name="using-wua-to-scan-for-updates-offline"></a>Использование агента WUA для проверки наличия обновлений в автономном режиме

Агент Центр обновления Windows (WUA) можно использовать для проверки компьютеров на наличие обновлений безопасности без подключения к Центр обновления Windows или серверу Windows Server Update Services (WSUS), что позволяет проверять наличие обновлений безопасности на компьютерах, которые не подключены к Интернету.

Для автономного сканирования на наличие обновлений требуется скачивание подписанного файла Wsusscn2.cab из Центр обновления Windows.

Файл Wsusscn2.cab — это CAB-файл, подписанный корпорацией Майкрософт. Этот файл содержит сведения об обновлениях, связанных с безопасностью, опубликованных корпорацией Майкрософт. Компьютеры, не подключенные к Интернету, могут быть проверены на наличие или необходимость наличия обновлений, связанных с безопасностью. Файл Wsusscn2.cab не содержит обновлений для системы безопасности, поэтому необходимо получить и установить все необходимые обновления для системы безопасности с помощью других средств. Новые версии файла Wsusscn2.cab периодически выпускаются, так как обновления, связанные с безопасностью, выпускаются, удаляются или изменяются на сайте Центр обновления Windows. Последний файл Wsusscn2.cab доступен для загрузки в следующем расположении: [скачать Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)

После загрузки последней версии Wsusscn2.cab файл может быть предоставлен методу [**аддсканпаккажесервице**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) , а API WUA можно использовать для поиска обновлений безопасности на автономном компьютере. WUA проверяет, подписано Wsusscn2.cab действительным сертификатом Майкрософт перед запуском автономной проверки.

> [!NOTE]
> В соответствии с нашей [инициативой по устаревшей SHA-1](https://aka.ms/sha1deprecation)файл Wsusscn2.cab больше не является двойной подписью с помощью SHA-1 и набора алгоритмов хэширования SHA-2 (в частности sha-256). Теперь этот файл подписан только с помощью SHA-256. Администраторы, которые проверяют цифровые подписи в этом файле, теперь должны иметь только отдельные подписи SHA-256.

## <a name="example"></a>Пример

В следующем примере файл Wsusscn2.cab используется для сканирования компьютера и отображения отсутствующих обновлений.

> [!IMPORTANT]
> Этот сценарий предназначен для демонстрации использования API-интерфейсов агента Центр обновления Windows и предоставления примера того, как разработчики могут использовать эти API для решения проблем. Этот сценарий не предназначен для рабочего кода, и сам сценарий не поддерживается корпорацией Майкрософт (хотя поддерживаются базовые API-интерфейсы Центр обновления Windows агента).

 


```VB
Set UpdateSession = CreateObject("Microsoft.Update.Session")
Set UpdateServiceManager = CreateObject("Microsoft.Update.ServiceManager")
Set UpdateService = UpdateServiceManager.AddScanPackageService("Offline Sync Service", "c:\wsusscn2.cab", 1)
Set UpdateSearcher = UpdateSession.CreateUpdateSearcher()

WScript.Echo "Searching for updates..." & vbCRLF

UpdateSearcher.ServerSelection = 3 ' ssOthers

UpdateSearcher.ServiceID = UpdateService.ServiceID

Set SearchResult = UpdateSearcher.Search("IsInstalled=0")

Set Updates = SearchResult.Updates

If searchResult.Updates.Count = 0 Then
    WScript.Echo "There are no applicable updates."
    WScript.Quit
End If

WScript.Echo "List of applicable items on the machine when using wssuscan.cab:" & vbCRLF

For I = 0 to searchResult.Updates.Count-1
    Set update = searchResult.Updates.Item(I)
    WScript.Echo I + 1 & "> " & update.Title
Next

WScript.Quit
```



 

 



