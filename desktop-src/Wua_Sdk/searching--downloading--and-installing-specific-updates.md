---
description: В примере сценариев в этом разделе показано, как использовать агент Центр обновления Windows (WUA) для проверки, загрузки и установки определенного обновления. Обновление можно указать по его названию.
ms.assetid: 4a5bb920-fc51-48a0-8f66-bb2fcc72589f
title: Поиск, скачивание и установка конкретных обновлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aadd7903303356c3937f41e44aa7a47e71192409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343805"
---
# <a name="searching-downloading-and-installing-specific-updates"></a><span data-ttu-id="68c9a-104">Поиск, скачивание и установка конкретных обновлений</span><span class="sxs-lookup"><span data-stu-id="68c9a-104">Searching, Downloading, and Installing Specific Updates</span></span>

<span data-ttu-id="68c9a-105">В примере сценариев в этом разделе показано, как использовать агент Центр обновления Windows (WUA) для проверки, загрузки и установки определенного обновления.</span><span class="sxs-lookup"><span data-stu-id="68c9a-105">The scripting sample in this topic shows you how to use the Windows Update Agent (WUA) to scan, download, and install a specific update.</span></span> <span data-ttu-id="68c9a-106">Обновление можно указать по его названию.</span><span class="sxs-lookup"><span data-stu-id="68c9a-106">The update can be specified by its title.</span></span>

<span data-ttu-id="68c9a-107">В примере выполняется поиск определенного обновления программного обеспечения, скачивается обновление, а затем устанавливается обновление.</span><span class="sxs-lookup"><span data-stu-id="68c9a-107">The sample searches for a specific software update, downloads the update, and then installs the update.</span></span> <span data-ttu-id="68c9a-108">Например, пользователь может использовать этот метод, чтобы определить, установлено ли на компьютере критическое обновление для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="68c9a-108">For example, a user can use this method to determine if a critical security update is installed on a computer.</span></span> <span data-ttu-id="68c9a-109">Если обновление не установлено, пользователь может убедиться, что обновление загружено и установлено.</span><span class="sxs-lookup"><span data-stu-id="68c9a-109">If the update isn't installed, the user can ensure that the update is downloaded and installed.</span></span> <span data-ttu-id="68c9a-110">Пользователь также может убедиться, что они получают уведомления о состоянии установки.</span><span class="sxs-lookup"><span data-stu-id="68c9a-110">The user can also ensure that they are notified about the status of the installation.</span></span>

<span data-ttu-id="68c9a-111">Образец обновления определяется [**свойством Title в заголовке иупдате**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title).</span><span class="sxs-lookup"><span data-stu-id="68c9a-111">The sample update is identified by the update title in [**Title Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title).</span></span> <span data-ttu-id="68c9a-112">В этом примере предлагается обновление для клиента Windows Rights Management Client 1,0.</span><span class="sxs-lookup"><span data-stu-id="68c9a-112">The title of the update that is suggested in this sample is "Update for Windows Rights Management client 1.0."</span></span>

> [!Note]  
> <span data-ttu-id="68c9a-113">Сведения о поиске, скачивании и установке всех обновлений, применимых к конкретному приложению, см. в разделе [Поиск, скачивание и установка обновлений](searching--downloading--and-installing-updates.md).</span><span class="sxs-lookup"><span data-stu-id="68c9a-113">For info about how to search, download, and install all the updates that apply to a specific application, see [Searching, Downloading, and Installing Updates](searching--downloading--and-installing-updates.md).</span></span>

 

<span data-ttu-id="68c9a-114">Прежде чем пытаться выполнить этот пример, обратите внимание на следующее:</span><span class="sxs-lookup"><span data-stu-id="68c9a-114">Before you attempt to run this sample, note the following:</span></span>

-   <span data-ttu-id="68c9a-115">На компьютере должен быть установлен WUA.</span><span class="sxs-lookup"><span data-stu-id="68c9a-115">WUA must be installed on the computer.</span></span> <span data-ttu-id="68c9a-116">Дополнительные сведения о том, как определить версию установленного агента WUA, см. [в разделе Определение текущей версии WUA](determining-the-current-version-of-wua.md).</span><span class="sxs-lookup"><span data-stu-id="68c9a-116">For more info about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>
-   <span data-ttu-id="68c9a-117">Образец не предоставляет собственный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="68c9a-117">The sample doesn't provide its own user interface.</span></span> <span data-ttu-id="68c9a-118">WUA предлагает пользователю перезагрузить компьютер, если обновление требует перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="68c9a-118">WUA prompts the user to restart the computer if an update requires a restart.</span></span>
-   <span data-ttu-id="68c9a-119">Пример может скачивать обновления только из WUA.</span><span class="sxs-lookup"><span data-stu-id="68c9a-119">The sample can download updates only from WUA.</span></span> <span data-ttu-id="68c9a-120">Он не может скачивать обновления с сервера SUS 1,0.</span><span class="sxs-lookup"><span data-stu-id="68c9a-120">It can't download updates from a Software Update Services (SUS) 1.0 server.</span></span>
-   <span data-ttu-id="68c9a-121">Для работы с этим примером требуется сервер сценариев Windows (WSH).</span><span class="sxs-lookup"><span data-stu-id="68c9a-121">Running this sample requires Windows Script Host (WSH).</span></span> <span data-ttu-id="68c9a-122">Дополнительные сведения о WSH см. в разделе WSH раздела Software Development Kit (пакет SDK для платформы).</span><span class="sxs-lookup"><span data-stu-id="68c9a-122">For more info about WSH, see the WSH section of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="68c9a-123">Если образец копируется в файл с именем WUA \_SpecificUpdate.vbs, его можно запустить, открыв окно командной строки и введя следующую команду: **cscript WUA \_SpecificUpdate.vbs**</span><span class="sxs-lookup"><span data-stu-id="68c9a-123">If the sample is copied to a file named WUA\_SpecificUpdate.vbs, you can run it by opening a Command Prompt window and by typing this command: **cscript WUA\_SpecificUpdate.vbs**</span></span>  
    

## <a name="example"></a><span data-ttu-id="68c9a-124">Пример</span><span class="sxs-lookup"><span data-stu-id="68c9a-124">Example</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68c9a-125">Этот сценарий предназначен для демонстрации использования API-интерфейсов агента Центр обновления Windows и предоставления примера того, как разработчики могут использовать эти API для решения проблем.</span><span class="sxs-lookup"><span data-stu-id="68c9a-125">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="68c9a-126">Этот сценарий не предназначен для рабочего кода, и сам сценарий не поддерживается корпорацией Майкрософт (хотя поддерживаются базовые API-интерфейсы Центр обновления Windows агента).</span><span class="sxs-lookup"><span data-stu-id="68c9a-126">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


```VB
Set updateSession = CreateObject("Microsoft.Update.Session")
updateSession.ClientApplicationID = "MSDN Sample Script"

'Get update title to search for
WScript.Echo "Enter the title of the update: " & _
"(for example, Update for Windows Rights Management client 1.0)"
updateTitle = WScript.StdIn.Readline

WScript.Echo vbCRLF & "Searching for: " & updateTitle & "..."

Set updateSearcher = updateSession.CreateupdateSearcher()

'Search for all software updates, already installed and not installed
Set searchResult = _
updateSearcher.Search("Type='Software'")

Set updateToInstall = CreateObject("Microsoft.Update.UpdateColl")

updateIsApplicable = False

'Cycle through search results to look for the update title
For i = 0 To searchResult.Updates.Count-1
   Set update = searchResult.Updates.Item(i)
   If UCase(update.Title) = UCase(updateTitle) Then
   'Update in list of applicable updates 
   'Determine if it is already installed or not
      If update.IsInstalled = False Then
         WScript.Echo vbCRLF & _
         "Result: Update applicable, not installed."
         updateIsApplicable = True
         updateToInstall.Add(update)
      Else 
         'Update is installed so notify user and quit
         WScript.Echo vbCRLF & _
         "Result: Update applicable, already installed."
         updateIsApplicable = True
         WScript.Quit 
      End If
   End If 
Next

If updateIsApplicable = False Then
   WScript.Echo "Result: Update is not applicable to this machine."
   WScript.Quit
End If

WScript.Echo vbCRLF & "Would you like to install now? (Y/N)"
stdInput = WScript.StdIn.Readline
 
If (strInput = "N" or strInput = "n") Then 
   WScript.Quit
ElseIf  (stdInput = "Y" OR stdInput = "y") Then
   'Download update
   Set downloader = updateSession.CreateUpdateDownloader() 
   downloader.Updates = updateToInstall
   WScript.Echo vbCRLF & "Downloading..."
   Set downloadResult = downloader.Download()
   WScript.Echo "Download Result: " & downloadResult.ResultCode
  
   'Install Update
   Set installer = updateSession.CreateUpdateInstaller()
   WScript.Echo vbCRLF & "Installing..."
   installer.Updates = updateToInstall
   Set installationResult = installer.Install()
  
   'Output the result of the installation
   WScript.Echo "Installation Result: " & _
   installationResult.ResultCode
   WScript.Echo "Reboot Required: " & _
   installationResult.RebootRequired 
End If
```



 

 



