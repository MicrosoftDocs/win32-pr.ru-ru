---
title: Получение функций
description: Функции сетевого управления Get получают сведения о домене. Эти функции также можно вызывать для получения сведений о локальных, глобальных, рабочих станциях и учетных записях пользователя сервера.
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532237"
---
# <a name="get-functions"></a><span data-ttu-id="32b72-104">Получение функций</span><span class="sxs-lookup"><span data-stu-id="32b72-104">Get Functions</span></span>

<span data-ttu-id="32b72-105">Функции сетевого управления Get получают сведения о домене.</span><span class="sxs-lookup"><span data-stu-id="32b72-105">The network management get functions retrieve information about a domain.</span></span> <span data-ttu-id="32b72-106">Эти функции также можно вызывать для получения сведений о локальных, глобальных, рабочих станциях и учетных записях пользователя сервера.</span><span class="sxs-lookup"><span data-stu-id="32b72-106">You can also call these functions to retrieve information about local, global, workstation, and server user accounts.</span></span>

<span data-ttu-id="32b72-107">Ниже перечислены функции Get для управления сетью.</span><span class="sxs-lookup"><span data-stu-id="32b72-107">The network management get functions are listed following.</span></span>



| <span data-ttu-id="32b72-108">Функция</span><span class="sxs-lookup"><span data-stu-id="32b72-108">Function</span></span>                                                               | <span data-ttu-id="32b72-109">Описание</span><span class="sxs-lookup"><span data-stu-id="32b72-109">Description</span></span>                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32b72-110">**нетжетанидкнаме**</span><span class="sxs-lookup"><span data-stu-id="32b72-110">**NetGetAnyDCName**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | <span data-ttu-id="32b72-111">Возвращает имя любого контроллера домена для домена, который напрямую является доверенным для указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="32b72-111">Returns the name of any domain controller for a domain that is directly trusted by a specified server.</span></span>                                   |
| [<span data-ttu-id="32b72-112">**нетжетдкнаме**</span><span class="sxs-lookup"><span data-stu-id="32b72-112">**NetGetDCName**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | <span data-ttu-id="32b72-113">Возвращает имя основного контроллера домена (PDC) для указанного домена.</span><span class="sxs-lookup"><span data-stu-id="32b72-113">Returns the name of the primary domain controller (PDC) for the specified domain.</span></span>                                                        |
| [<span data-ttu-id="32b72-114">**нетжетдисплайинформатиониндекс**</span><span class="sxs-lookup"><span data-stu-id="32b72-114">**NetGetDisplayInformationIndex**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | <span data-ttu-id="32b72-115">Возвращает индекс первой записи отображаемой информации, имя которой начинается с указанной строки или в алфавитном порядке за строкой.</span><span class="sxs-lookup"><span data-stu-id="32b72-115">Returns the index of the first display information entry whose name begins with a specified string or alphabetically follows the string.</span></span> |
| [<span data-ttu-id="32b72-116">**неткуеридисплайинформатион**</span><span class="sxs-lookup"><span data-stu-id="32b72-116">**NetQueryDisplayInformation**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | <span data-ttu-id="32b72-117">Возвращает сведения об учетной записи пользователя, компьютера или глобальной группы.</span><span class="sxs-lookup"><span data-stu-id="32b72-117">Returns user, computer, or global group account information.</span></span>                                                                             |



 

<span data-ttu-id="32b72-118">Сведения, возвращаемые функцией [**неткуеридисплайинформатион**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) , доступны на следующих уровнях:</span><span class="sxs-lookup"><span data-stu-id="32b72-118">The information returned by the [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) function is available at the following levels:</span></span>

-   [<span data-ttu-id="32b72-119">**\_Группа дисплеев NET \_**</span><span class="sxs-lookup"><span data-stu-id="32b72-119">**NET\_DISPLAY\_GROUP**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [<span data-ttu-id="32b72-120">**NET \_ диспле \_ компьютера**</span><span class="sxs-lookup"><span data-stu-id="32b72-120">**NET\_DISPLAY\_MACHINE**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [<span data-ttu-id="32b72-121">**\_пользователь NET дисплея \_**</span><span class="sxs-lookup"><span data-stu-id="32b72-121">**NET\_DISPLAY\_USER**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 




