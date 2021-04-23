---
description: 'Выпуск VSS для Windows Server 2003 больше не поддерживает следующее:'
ms.assetid: 01993cae-433e-4d01-b805-f97592369575
title: Функции, удаленные из Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181d053420f0fc947ebad024c0eaf2bbaf32f3e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692923"
---
# <a name="functionality-removed-from-windows-server-2003"></a><span data-ttu-id="3bc47-103">Функции, удаленные из Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3bc47-103">Functionality Removed From Windows Server 2003</span></span>

<span data-ttu-id="3bc47-104">Выпуск VSS для Windows Server 2003 больше не поддерживает следующее:</span><span class="sxs-lookup"><span data-stu-id="3bc47-104">The Windows Server 2003 release of VSS no longer supports the following:</span></span>

-   <span data-ttu-id="3bc47-105">Модули записи не могут указывать новые назначения восстановления файлов ([*новые целевые расположения*](vssgloss-n.md)) в операциях восстановления.</span><span class="sxs-lookup"><span data-stu-id="3bc47-105">Writers cannot specify new file restore destinations ([*new target locations*](vssgloss-n.md)) at restore operations.</span></span>
-   <span data-ttu-id="3bc47-106">Повторное подключение доступной теневой копии в качестве тома с возможностью записи больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3bc47-106">Remounting an exposed shadow copy as a writable volume is no longer supported.</span></span> <span data-ttu-id="3bc47-107">Метод **ивссбаккупкомпонентс:: ремаунтреадврите** больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="3bc47-107">The **IVssBackupComponents::RemountReadWrite** method is no longer available.</span></span>
-   <span data-ttu-id="3bc47-108">Модули записи не могут указывать явно включаемые файлы (с помощью [**ивсскреатевритерметадата:: аддинклудефилес**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)).</span><span class="sxs-lookup"><span data-stu-id="3bc47-108">Writers cannot specify explicitly included files (using [**IVssCreateWriterMetadata::AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)).</span></span> <span data-ttu-id="3bc47-109">Файлы можно добавлять в компонент только в составе набора файлов с помощью [**ивсскреатевритерметадата:: аддфилестофилеграуп**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**Ивсскреатевритерметадата:: адддатабасефилес**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)или [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).</span><span class="sxs-lookup"><span data-stu-id="3bc47-109">Files can be added to a component only as part of a file set by using [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), or [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).</span></span>

    <span data-ttu-id="3bc47-110">Файлы по-прежнему можно явно исключить из компонента с помощью [**ивсскреатевритерметадата:: аддексклудефилес**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).</span><span class="sxs-lookup"><span data-stu-id="3bc47-110">Files can still be explicitly excluded from a component by using [**IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).</span></span>

 

 



