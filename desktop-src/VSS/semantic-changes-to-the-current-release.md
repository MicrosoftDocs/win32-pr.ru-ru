---
description: 'Сочетание пути, спецификации файла и флага рекурсии (Всзпас, Всзфилеспек и Брекурсиве соответственно) должны соответствовать одному из наборов файлов, добавленных в один из компонентов модуля записи с помощью Ивсскреатевритерметадата:: Аддфилестофилеграуп, Ивсскреатевритерметадата:: AddDatabaseFiles или IVssCreateWriterMetadata:: AddDatabaseLogFiles, если:'
ms.assetid: debf181a-1579-46f2-86ef-a1d2a850e99e
title: Семантические изменения в Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9d2edc56f215f554b497eebff9f76a1da53dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264021"
---
# <a name="semantic-changes-to-windows-server-2003"></a><span data-ttu-id="e249e-103">Семантические изменения в Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e249e-103">Semantic Changes to Windows Server 2003</span></span>

<span data-ttu-id="e249e-104">Сочетание пути, спецификации файла и флага рекурсии (*всзпас*, *всзфилеспек* и *брекурсиве* соответственно) должны соответствовать одному из наборов файлов, добавленных в один из компонентов модуля записи с помощью [**ивсскреатевритерметадата:: Аддфилестофилеграуп**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**ивсскреатевритерметадата:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)или [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) , если:</span><span class="sxs-lookup"><span data-stu-id="e249e-104">The combination of path, file specification, and recursion flag (*wszPath*, *wszFileSpec*, and *bRecursive*, respectively) must match that of one of the file sets added to one of the writer's components using [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), or [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) when:</span></span>

-   <span data-ttu-id="e249e-105">Инициатор запроса добавляет новый целевой объект с помощью [**ивссбаккупкомпонентс:: аддневтаржет**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).</span><span class="sxs-lookup"><span data-stu-id="e249e-105">A requester adds a new target using [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).</span></span>
-   <span data-ttu-id="e249e-106">Модуль записи добавляет сопоставление альтернативного расположения с помощью [**ивсскреатевритерметадата:: аддалтернателокатионмаппинг**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping).</span><span class="sxs-lookup"><span data-stu-id="e249e-106">A writer adds an alternate location mapping using [**IVssCreateWriterMetadata::AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping).</span></span>
-   <span data-ttu-id="e249e-107">Существующие файлы добавляются в виде различных файлов с помощью [**ивсскомпонент:: адддифференцедфилесбиластмодифитиме**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime).</span><span class="sxs-lookup"><span data-stu-id="e249e-107">Existing files are added as differenced files using [**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime).</span></span>
-   <span data-ttu-id="e249e-108">Инициатор запроса указывает, что для восстановления набора файлов с помощью [**ивссбаккупкомпонентс:: аддалтернативелокатионмаппинг**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)использовалось сопоставление альтернативного расположения.</span><span class="sxs-lookup"><span data-stu-id="e249e-108">A requester indicates that an alternate location mapping was used to restore a file set using [**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping).</span></span>

 

 



