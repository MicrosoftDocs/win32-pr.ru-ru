---
description: Защита ресурсов Windows (WRP) предотвращает замену необходимых системных файлов, папок и разделов реестра, установленных в составе Windows Vista или Windows Server 2008.
ms.assetid: 1cb67b4a-dc75-4bd7-b314-d695c10d5558
title: Обнаружение замены ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62dc1855b98ca5834ef9e13e2f48bf7cca492e94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817040"
---
# <a name="detecting-resource-replacement"></a><span data-ttu-id="c9629-103">Обнаружение замены ресурсов</span><span class="sxs-lookup"><span data-stu-id="c9629-103">Detecting Resource Replacement</span></span>

<span data-ttu-id="c9629-104">Защита ресурсов Windows (WRP) предотвращает замену необходимых системных файлов, папок и разделов реестра, установленных в составе Windows Vista или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c9629-104">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of Windows Vista or Windows Server 2008.</span></span>

<span data-ttu-id="c9629-105">WRP защищает файлы, папки и разделы реестра в Windows Vista или Windows Server 2008, выявляя и предотвращая попытки замены защищенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c9629-105">WRP protects files, folders, and registry keys on Windows Vista or Windows Server 2008 by detecting and preventing attempts to replace protected resources.</span></span> <span data-ttu-id="c9629-106">Эта защита основана на списке управления доступом на уровне пользователей Windows (DACL) и списках управления доступом (ACL), определенных для защищенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c9629-106">This protection is based on a Windows discretionary access control list (DACL) and access control lists (ACL) defined for protected resources.</span></span> <span data-ttu-id="c9629-107">Разрешение на полный доступ для изменения ресурсов, защищенных WRP, ограничено TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="c9629-107">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="c9629-108">Ресурсы, защищенные WRP, можно изменять только с помощью [поддерживаемых механизмов замены ресурсов](supported-file-replacement-mechanisms.md) в службе установщика модулей Windows.</span><span class="sxs-lookup"><span data-stu-id="c9629-108">WRP-protected resources can only be changed using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span> <span data-ttu-id="c9629-109">Приложения, пытающиеся изменить ресурс, защищенный WRP, никогда не изменяют ресурс и могут получить сообщение об ошибке, сообщающее, что доступ к ресурсу запрещен.</span><span class="sxs-lookup"><span data-stu-id="c9629-109">Applications attempting to modify a WRP-protected resource never change the resource and may receive an error message that states that access to the resource was denied.</span></span>

<span data-ttu-id="c9629-110">Приложения и установщики могут использовать функции [**сфЦисфилепротектед**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) и [**сфЦискэйпротектед**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) , чтобы определить, защищен ли файл или раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="c9629-110">Applications and installers can use the [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) and [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) functions to determine whether a file or registry key is protected.</span></span>

<span data-ttu-id="c9629-111">\* \* Windows Server 2003 и Windows XP: \* \*</span><span class="sxs-lookup"><span data-stu-id="c9629-111">\*\*Windows Server 2003 and Windows XP:  \*\*</span></span>

<span data-ttu-id="c9629-112">Защита файлов Windows (WFP) защищает системные файлы путем обнаружения попыток замены защищенных системных файлов.</span><span class="sxs-lookup"><span data-stu-id="c9629-112">Windows File Protection (WFP) protects system files by detecting attempts to replace protected system files.</span></span> <span data-ttu-id="c9629-113">Эта защита активируется после того, как WFP получает уведомление об изменении каталога для файла в защищенном каталоге.</span><span class="sxs-lookup"><span data-stu-id="c9629-113">This protection is triggered after WFP receives a directory change notification for a file in a protected directory.</span></span> <span data-ttu-id="c9629-114">Когда WFP получает это уведомление, он определяет, какой файл был изменен.</span><span class="sxs-lookup"><span data-stu-id="c9629-114">When WFP receives this notification, it determines which file has changed.</span></span> <span data-ttu-id="c9629-115">Если файл защищен, WFP ищет подпись файла в файле каталога, чтобы определить, является ли новый файл правильной версией.</span><span class="sxs-lookup"><span data-stu-id="c9629-115">If the file is protected, WFP looks up the file signature in a catalog file to determine if the new file is the correct version.</span></span> <span data-ttu-id="c9629-116">Если версия файла неверна, система заменяет файл правильной версией из кэша или с носителя распространения в зависимости от того, находится ли файл в кэше.</span><span class="sxs-lookup"><span data-stu-id="c9629-116">If the file version is not correct, the system replaces the file with the correct version from either the cache or distribution media, depending on whether the file is located in the cache.</span></span> <span data-ttu-id="c9629-117">WFP ищет правильный файл в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="c9629-117">WFP searches for the correct file in the following order:</span></span>

1.  <span data-ttu-id="c9629-118">Поиск в каталоге кэша.</span><span class="sxs-lookup"><span data-stu-id="c9629-118">Search the cache directory.</span></span>
2.  <span data-ttu-id="c9629-119">Поиск пути сетевой установки, если система была установлена с помощью сетевой установки.</span><span class="sxs-lookup"><span data-stu-id="c9629-119">Search the network install path, if the system was installed using network install.</span></span>
3.  <span data-ttu-id="c9629-120">Поиск на компакт-диске Windows, если система была установлена с компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="c9629-120">Search on a Windows CD-ROM, if the system was installed from CD-ROM.</span></span>

<span data-ttu-id="c9629-121">Если WFP не может автоматически найти файл в первых двух местах, отображается следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="c9629-121">If WFP cannot automatically find the file in the first two locations, it displays the following message:</span></span>

![сообщение WFP, отображаемое, если файл не найден в каталоге кэша или пути сетевой установки](images/wfp-1.png)

<span data-ttu-id="c9629-123">Если система была установлена с помощью компакт-диска, WFP отображает следующее сообщение:</span><span class="sxs-lookup"><span data-stu-id="c9629-123">If the system was installed using a CD-ROM, WFP displays the following message:</span></span>

![отображается сообщение WFP, предлагающее пользователю вставить компакт-диск Windows](images/wfp-2.png)

<span data-ttu-id="c9629-125">Если администратор не вошел в систему, WFP не сможет отобразить какое-либо из этих диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="c9629-125">If an administrator is not logged on, WFP cannot display either of these dialog boxes.</span></span> <span data-ttu-id="c9629-126">WFP отобразит диалоговое окно после входа администратора в систему.</span><span class="sxs-lookup"><span data-stu-id="c9629-126">WFP will display the dialog box after an administrator logs on.</span></span>

<span data-ttu-id="c9629-127">WFP также регистрирует попытки замены файлов в журнале системных событий.</span><span class="sxs-lookup"><span data-stu-id="c9629-127">WFP also logs the file replacement attempt in the system event log.</span></span> <span data-ttu-id="c9629-128">Если администратор отменил восстановление правильного файла, WFP регистрирует отмену.</span><span class="sxs-lookup"><span data-stu-id="c9629-128">If the administrator canceled restoration of the correct file, WFP logs the cancellation.</span></span>

## <a name="retrieving-the-list-of-protected-files"></a><span data-ttu-id="c9629-129">Получение списка защищенных файлов</span><span class="sxs-lookup"><span data-stu-id="c9629-129">Retrieving the List of Protected Files</span></span>

<span data-ttu-id="c9629-130">В следующем примере показано, как приложения и установщики могут использовать функцию [**сфкжетнекстпротектедфиле**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) для получения полного списка защищенных файлов.</span><span class="sxs-lookup"><span data-stu-id="c9629-130">The following example shows how applications and installers can use the [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) function to get the complete list of protected files.</span></span>


```C++
#include <windows.h>
#include <sfc.h>
#include <stdio.h>

#pragma comment(lib, "sfc")

void wmain (int argc, WCHAR ** argv)
{  UNREFERENCED_PARAMETER(argc);    
   PROTECTED_FILE_DATA pfd = {0};
   BOOL fResult;

   wprintf (L"List of protected files:\n\n", argv[1]);

   while (FALSE != (fResult = SfcGetNextProtectedFile (NULL, &pfd)))
   {
      wprintf (L"   %lu   %s\n", pfd.FileNumber, pfd.FileName);
   }

   if (GetLastError() == ERROR_NO_MORE_FILES)
   {
      wprintf (L"\nAll %lu protected files listed\n", pfd.FileNumber);
   }
   else
   {
      wprintf (L"\nerror %lu: SfcGetNextProtectedFile() failed unexpectedly\n", GetLastError());
   }

}
```



 

 



