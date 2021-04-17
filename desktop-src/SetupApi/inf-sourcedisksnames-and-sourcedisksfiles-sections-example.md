---
description: Раздел Саурцедискснамес INF-файла определяет диски, содержащие исходные файлы, которые устанавливаются.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: Примеры разделов Саурцедискснамес и Саурцедисксфилес в INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f991727a8a2ca9cce2bd2d7161dfbf27b62ce74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663902"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a><span data-ttu-id="d314f-103">Примеры разделов Саурцедискснамес и Саурцедисксфилес в INF</span><span class="sxs-lookup"><span data-stu-id="d314f-103">INF SourceDisksNames and SourceDisksFiles Sections Example</span></span>

<span data-ttu-id="d314f-104">Раздел **САУРЦЕДИСКСНАМЕС** INF-файла определяет диски, содержащие исходные файлы, которые устанавливаются.</span><span class="sxs-lookup"><span data-stu-id="d314f-104">The **SourceDisksNames** section of an INF file identifies the disks that contain the source files being installed.</span></span> <span data-ttu-id="d314f-105">Раздел **саурцедисксфилес** определяет исходные файлы и исходные диски, содержащие их.</span><span class="sxs-lookup"><span data-stu-id="d314f-105">The **SourceDisksFiles** section identifies the source files and the source disks that contain them.</span></span> <span data-ttu-id="d314f-106">Обратите внимание, что платформы MIPS, Alpha и PPC не поддерживаются в Windows 2000 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d314f-106">Note that MIPS, Alpha, and PPC platforms are not supported by Windows 2000 or Windows XP.</span></span>

<span data-ttu-id="d314f-107">Начиная с Windows XP, в разделе **саурцедискснамес** может быть указан тег и CAB-файл.</span><span class="sxs-lookup"><span data-stu-id="d314f-107">Beginning with Windows XP, a **SourceDisksNames** section may specify a tag as well as cabinet file.</span></span> <span data-ttu-id="d314f-108">Например, следующий раздел **саурцедискснамес** может использоваться с съемными или стационарными носителями.</span><span class="sxs-lookup"><span data-stu-id="d314f-108">For example, the following **SourceDisksNames** section may be used with removable or fixed media.</span></span> <span data-ttu-id="d314f-109">При использовании съемного носителя раздел пример проверяет наличие носителя, сначала проверяя наличие тега.</span><span class="sxs-lookup"><span data-stu-id="d314f-109">If using removable media, the example section verifies the presence of the media by first checking for the presence of the tag.</span></span> <span data-ttu-id="d314f-110">Если используется фиксированный носитель, в разделе пример для проверки наличия носителя сначала проверяется наличие CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="d314f-110">If using fixed media, the example section verifies the presence of the media by first checking for the presence of the cabinet.</span></span> <span data-ttu-id="d314f-111">После проверки наличия CAB-файла система пытается скопировать файлы из CAB-файла и запрашивает файлы, которые не удалось скопировать.</span><span class="sxs-lookup"><span data-stu-id="d314f-111">After verifying the presence of a cabinet, the system attempts to copy files out of the cabinet and prompts for any files it was unable to copy.</span></span>

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

<span data-ttu-id="d314f-112">Дополнительные сведения о **саурцедискснамес** или **саурцедисксфилес** см. в разделах «Общие рекомендации по INF-файлу» и «разделы и директивы INF-файла» пакета средств разработки драйверов Microsoft Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d314f-112">For more information about **SourceDisksNames** or **SourceDisksFiles**, see the "General Guidelines for INF File" and "INF File Sections and Directives" sections of the Microsoft Windows 2000 Driver Development Kit.</span></span>

 

 



