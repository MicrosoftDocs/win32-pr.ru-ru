---
description: 'Для определения установщик Windows версии можно использовать следующие методы:'
ms.assetid: 6b39bb19-4360-4d0e-a797-980912a91275
title: Определение версии установщик Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a48434fe415084a93158fb3445a36906d8b8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663711"
---
# <a name="determining-the-windows-installer-version"></a><span data-ttu-id="a6c1d-103">Определение версии установщик Windows</span><span class="sxs-lookup"><span data-stu-id="a6c1d-103">Determining the Windows Installer Version</span></span>

<span data-ttu-id="a6c1d-104">Для определения установщик Windows версии можно использовать следующие методы:</span><span class="sxs-lookup"><span data-stu-id="a6c1d-104">You can use the following methods to determine the Windows Installer version:</span></span>

-   <span data-ttu-id="a6c1d-105">Вызовите функцию [**мсижетфилеверсион**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) с параметром *сзфилепас* , для которого задан путь к файлу Msi.dll.</span><span class="sxs-lookup"><span data-stu-id="a6c1d-105">Call the [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) function with the *szFilePath* parameter set to the path to the file Msi.dll.</span></span>

    <span data-ttu-id="a6c1d-106">Вы можете вызвать функцию [**шжеткновнфолдерпас**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) с **\_ системной** константой CSid, чтобы получить путь к Msi.dll.</span><span class="sxs-lookup"><span data-stu-id="a6c1d-106">You can call the [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function with the **CSIDL\_SYSTEM** constant to get the path to Msi.dll.</span></span> <span data-ttu-id="a6c1d-107">Начиная с Windows Vista, приложения должны использовать функцию [**шжетфолдерпас**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) и **рефкновнфолдерид** "System".</span><span class="sxs-lookup"><span data-stu-id="a6c1d-107">Beginning with Windows Vista, applications should use the [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) function and the **REFKNOWNFOLDERID** "System."</span></span> <span data-ttu-id="a6c1d-108">Существующие приложения, использующие функцию **шжетфолдерпас** и тип **CSid** , продолжат работать.</span><span class="sxs-lookup"><span data-stu-id="a6c1d-108">Existing applications that use the **SHGetFolderPath** function and the **CSIDL** type will continue to work.</span></span>

-   <span data-ttu-id="a6c1d-109">Значение свойства [**установщика. Version**](installer-version.md) [**объекта установщика**](installer-object.md) эквивалентно строкам из четырех полей, перечисленным в [выпущенных версиях установщик Windows](released-versions-of-windows-installer.md) разделе.</span><span class="sxs-lookup"><span data-stu-id="a6c1d-109">The value of the [**Installer.Version**](installer-version.md) property of the [**Installer Object**](installer-object.md) is equivalent to the four-field strings listed in the [Released Versions of Windows Installer](released-versions-of-windows-installer.md) topic.</span></span>
-   <span data-ttu-id="a6c1d-110">Приложения могут получить версию установщик Windows с помощью [**дллжетверсион**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="a6c1d-110">Applications can get the Windows Installer version by using [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).</span></span>
-   <span data-ttu-id="a6c1d-111">Установщик задает для свойства [**версионмси**](versionmsi.md) версию установщик Windows, которая выполняется во время установки.</span><span class="sxs-lookup"><span data-stu-id="a6c1d-111">The installer sets the [**VersionMsi**](versionmsi.md) property to the version of Windows Installer that is run during the installation.</span></span>

<span data-ttu-id="a6c1d-112">Дополнительные сведения см. в статье [Released Versions of установщик Windows](released-versions-of-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="a6c1d-112">For more information, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

 

 
