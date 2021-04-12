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
# <a name="using-wua-to-scan-for-updates-offline"></a><span data-ttu-id="28835-104">Использование агента WUA для проверки наличия обновлений в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="28835-104">Using WUA to Scan for Updates Offline</span></span>

<span data-ttu-id="28835-105">Агент Центр обновления Windows (WUA) можно использовать для проверки компьютеров на наличие обновлений безопасности без подключения к Центр обновления Windows или серверу Windows Server Update Services (WSUS), что позволяет проверять наличие обновлений безопасности на компьютерах, которые не подключены к Интернету.</span><span class="sxs-lookup"><span data-stu-id="28835-105">Windows Update Agent (WUA) can be used to scan computers for security updates without connecting to Windows Update or to a Windows Server Update Services (WSUS) server, which enables computers that are not connected to the Internet to be scanned for security updates.</span></span>

<span data-ttu-id="28835-106">Для автономного сканирования на наличие обновлений требуется скачивание подписанного файла Wsusscn2.cab из Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="28835-106">Offline scanning for updates requires the download of a signed file, Wsusscn2.cab, from Windows Update.</span></span>

<span data-ttu-id="28835-107">Файл Wsusscn2.cab — это CAB-файл, подписанный корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="28835-107">The Wsusscn2.cab file is a cabinet file that is signed by Microsoft.</span></span> <span data-ttu-id="28835-108">Этот файл содержит сведения об обновлениях, связанных с безопасностью, опубликованных корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="28835-108">This file contains info about security-related updates that are published by Microsoft.</span></span> <span data-ttu-id="28835-109">Компьютеры, не подключенные к Интернету, могут быть проверены на наличие или необходимость наличия обновлений, связанных с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="28835-109">Computers that aren't connected to the Internet can be scanned to see whether these security-related updates are present or required.</span></span> <span data-ttu-id="28835-110">Файл Wsusscn2.cab не содержит обновлений для системы безопасности, поэтому необходимо получить и установить все необходимые обновления для системы безопасности с помощью других средств.</span><span class="sxs-lookup"><span data-stu-id="28835-110">The Wsusscn2.cab file doesn't contain the security updates themselves so you must obtain and install any needed security-related updates through other means.</span></span> <span data-ttu-id="28835-111">Новые версии файла Wsusscn2.cab периодически выпускаются, так как обновления, связанные с безопасностью, выпускаются, удаляются или изменяются на сайте Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="28835-111">New versions of the Wsusscn2.cab file are released periodically as security-related updates are released, removed, or revised on the Windows Update site.</span></span> <span data-ttu-id="28835-112">Последний файл Wsusscn2.cab доступен для загрузки в следующем расположении: [скачать Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)</span><span class="sxs-lookup"><span data-stu-id="28835-112">The latest Wsusscn2.cab file is available for download at the following location: [Download Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)</span></span>

<span data-ttu-id="28835-113">После загрузки последней версии Wsusscn2.cab файл может быть предоставлен методу [**аддсканпаккажесервице**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) , а API WUA можно использовать для поиска обновлений безопасности на автономном компьютере.</span><span class="sxs-lookup"><span data-stu-id="28835-113">After you download the latest Wsusscn2.cab, the file can be provided to the [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) method, and the WUA API can be used to search the offline computer for security updates.</span></span> <span data-ttu-id="28835-114">WUA проверяет, подписано Wsusscn2.cab действительным сертификатом Майкрософт перед запуском автономной проверки.</span><span class="sxs-lookup"><span data-stu-id="28835-114">WUA validates that the Wsusscn2.cab is signed by a valid Microsoft certificate before running an offline scan.</span></span>

> [!NOTE]
> <span data-ttu-id="28835-115">В соответствии с нашей [инициативой по устаревшей SHA-1](https://aka.ms/sha1deprecation)файл Wsusscn2.cab больше не является двойной подписью с помощью SHA-1 и набора алгоритмов хэширования SHA-2 (в частности sha-256).</span><span class="sxs-lookup"><span data-stu-id="28835-115">In accordance with our [SHA-1 deprecation initiative](https://aka.ms/sha1deprecation), the Wsusscn2.cab file is no longer dual-signed using both SHA-1 and the SHA-2 suite of hash algorithms (specifically SHA-256).</span></span> <span data-ttu-id="28835-116">Теперь этот файл подписан только с помощью SHA-256.</span><span class="sxs-lookup"><span data-stu-id="28835-116">This file is now signed using only SHA-256.</span></span> <span data-ttu-id="28835-117">Администраторы, которые проверяют цифровые подписи в этом файле, теперь должны иметь только отдельные подписи SHA-256.</span><span class="sxs-lookup"><span data-stu-id="28835-117">Administrators who verify digital signatures on this file should now expect only single SHA-256 signatures.</span></span>

## <a name="example"></a><span data-ttu-id="28835-118">Пример</span><span class="sxs-lookup"><span data-stu-id="28835-118">Example</span></span>

<span data-ttu-id="28835-119">В следующем примере файл Wsusscn2.cab используется для сканирования компьютера и отображения отсутствующих обновлений.</span><span class="sxs-lookup"><span data-stu-id="28835-119">The following example uses the Wsusscn2.cab file to scan a computer and displays updates that are missing.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28835-120">Этот сценарий предназначен для демонстрации использования API-интерфейсов агента Центр обновления Windows и предоставления примера того, как разработчики могут использовать эти API для решения проблем.</span><span class="sxs-lookup"><span data-stu-id="28835-120">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="28835-121">Этот сценарий не предназначен для рабочего кода, и сам сценарий не поддерживается корпорацией Майкрософт (хотя поддерживаются базовые API-интерфейсы Центр обновления Windows агента).</span><span class="sxs-lookup"><span data-stu-id="28835-121">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


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



 

 



