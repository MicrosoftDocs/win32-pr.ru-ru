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
# <a name="searching-downloading-and-installing-specific-updates"></a>Поиск, скачивание и установка конкретных обновлений

В примере сценариев в этом разделе показано, как использовать агент Центр обновления Windows (WUA) для проверки, загрузки и установки определенного обновления. Обновление можно указать по его названию.

В примере выполняется поиск определенного обновления программного обеспечения, скачивается обновление, а затем устанавливается обновление. Например, пользователь может использовать этот метод, чтобы определить, установлено ли на компьютере критическое обновление для системы безопасности. Если обновление не установлено, пользователь может убедиться, что обновление загружено и установлено. Пользователь также может убедиться, что они получают уведомления о состоянии установки.

Образец обновления определяется [**свойством Title в заголовке иупдате**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title). В этом примере предлагается обновление для клиента Windows Rights Management Client 1,0.

> [!Note]  
> Сведения о поиске, скачивании и установке всех обновлений, применимых к конкретному приложению, см. в разделе [Поиск, скачивание и установка обновлений](searching--downloading--and-installing-updates.md).

 

Прежде чем пытаться выполнить этот пример, обратите внимание на следующее:

-   На компьютере должен быть установлен WUA. Дополнительные сведения о том, как определить версию установленного агента WUA, см. [в разделе Определение текущей версии WUA](determining-the-current-version-of-wua.md).
-   Образец не предоставляет собственный пользовательский интерфейс. WUA предлагает пользователю перезагрузить компьютер, если обновление требует перезагрузки.
-   Пример может скачивать обновления только из WUA. Он не может скачивать обновления с сервера SUS 1,0.
-   Для работы с этим примером требуется сервер сценариев Windows (WSH). Дополнительные сведения о WSH см. в разделе WSH раздела Software Development Kit (пакет SDK для платформы). Если образец копируется в файл с именем WUA \_SpecificUpdate.vbs, его можно запустить, открыв окно командной строки и введя следующую команду: **cscript WUA \_SpecificUpdate.vbs**  
    

## <a name="example"></a>Пример

> [!IMPORTANT]
> Этот сценарий предназначен для демонстрации использования API-интерфейсов агента Центр обновления Windows и предоставления примера того, как разработчики могут использовать эти API для решения проблем. Этот сценарий не предназначен для рабочего кода, и сам сценарий не поддерживается корпорацией Майкрософт (хотя поддерживаются базовые API-интерфейсы Центр обновления Windows агента).

 


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



 

 



