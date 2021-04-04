---
description: С функциями Сетупинсталлфиле, Сетупинсталлфиликс и Сетупинсталлфроминфсектион используются следующие уведомления. Дополнительные сведения о форматировании и использовании уведомлений см. в разделе уведомления.
ms.assetid: 095cf4c9-3cb9-4b95-a8a2-9312c134e721
title: Уведомления INF-файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f58863d48c1af809c0cbbcdc2d625214a6e90a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998619"
---
# <a name="inf-file-notifications"></a><span data-ttu-id="53cd6-104">Уведомления INF-файлов</span><span class="sxs-lookup"><span data-stu-id="53cd6-104">INF File Notifications</span></span>

<span data-ttu-id="53cd6-105">С функциями [**сетупинсталлфиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**сетупинсталлфиликс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)и [**сетупинсталлфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) используются следующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="53cd6-105">The following notifications are used with the [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa), and [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) functions.</span></span> <span data-ttu-id="53cd6-106">Дополнительные сведения о форматировании и использовании уведомлений см. в разделе [уведомления](notifications.md).</span><span class="sxs-lookup"><span data-stu-id="53cd6-106">For more information about the format and use of notifications, see [Notifications](notifications.md).</span></span>



| <span data-ttu-id="53cd6-107">Уведомление</span><span class="sxs-lookup"><span data-stu-id="53cd6-107">Notification</span></span>                                                      | <span data-ttu-id="53cd6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="53cd6-108">Description</span></span>                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="53cd6-109">**СПФИЛЕНОТИФИ \_ филеопделайед**</span><span class="sxs-lookup"><span data-stu-id="53cd6-109">**SPFILENOTIFY\_FILEOPDELAYED**</span></span>](spfilenotify-fileopdelayed.md) | <span data-ttu-id="53cd6-110">Файл используется, и текущая операция откладывается до перезагрузки системы.</span><span class="sxs-lookup"><span data-stu-id="53cd6-110">The file is in use, and the current operation is delayed until the system is rebooted.</span></span> |
| [<span data-ttu-id="53cd6-111">**СПФИЛЕНОТИФИ \_ лангмисматч**</span><span class="sxs-lookup"><span data-stu-id="53cd6-111">**SPFILENOTIFY\_LANGMISMATCH**</span></span>](spfilenotify-langmismatch.md)   | <span data-ttu-id="53cd6-112">Язык текущего файла не соответствует языку системы.</span><span class="sxs-lookup"><span data-stu-id="53cd6-112">The language of the current file does not match the system language.</span></span>                   |
| [<span data-ttu-id="53cd6-113">**СПФИЛЕНОТИФИ \_ таржетексистс**</span><span class="sxs-lookup"><span data-stu-id="53cd6-113">**SPFILENOTIFY\_TARGETEXISTS**</span></span>](spfilenotify-targetexists.md)   | <span data-ttu-id="53cd6-114">Копия указанного файла уже существует на целевом объекте.</span><span class="sxs-lookup"><span data-stu-id="53cd6-114">A copy of the specified file already exists on the target.</span></span>                             |
| [<span data-ttu-id="53cd6-115">**СПФИЛЕНОТИФИ \_ таржетневер**</span><span class="sxs-lookup"><span data-stu-id="53cd6-115">**SPFILENOTIFY\_TARGETNEWER**</span></span>](spfilenotify-targetnewer.md)     | <span data-ttu-id="53cd6-116">На целевом компьютере существует более новая версия указанного файла.</span><span class="sxs-lookup"><span data-stu-id="53cd6-116">A newer version of the specified file exists on the target.</span></span>                            |



 

> [!Note]  
> <span data-ttu-id="53cd6-117">Так как [**сетупинсталлфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) создает и фиксирует внутреннюю очередь файлов, она также использует [уведомления об очереди файлов](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="53cd6-117">Because [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) creates and commits an internal file queue, it also uses the [File Queue Notifications](file-queue-notifications.md).</span></span>

 

 

 



