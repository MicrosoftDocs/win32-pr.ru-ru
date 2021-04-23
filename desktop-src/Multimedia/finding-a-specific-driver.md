---
title: Поиск конкретного драйвера
description: Поиск конкретного драйвера
ms.assetid: d48dc313-4606-4f70-b2fe-ed99160e53fc
keywords:
- Диспетчер аудиосжатия (ACM), поиск драйверов
- ACM (диспетчер аудиосжатия), поиск драйверов
- Примеры ACM, поиск драйверов
- Поиск драйверов
- Функция Акмдриверенум
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d8e8198fdf3bc742c2705e1a83b3ea8036c80f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888991"
---
# <a name="finding-a-specific-driver"></a><span data-ttu-id="eccb4-108">Поиск конкретного драйвера</span><span class="sxs-lookup"><span data-stu-id="eccb4-108">Finding a Specific Driver</span></span>

<span data-ttu-id="eccb4-109">Может потребоваться, чтобы приложение отправляло сообщение непосредственно определенному драйверу или для обнаружения определенных драйверов из списка.</span><span class="sxs-lookup"><span data-stu-id="eccb4-109">You might want your application to send a message directly to a specific driver or to identify certain drivers from the list.</span></span> <span data-ttu-id="eccb4-110">Например, может потребоваться, чтобы приложение определяло драйверы, поддерживающие фильтры, а затем запрашивает каждый драйвер, чтобы определить, какие теги фильтров он поддерживает.</span><span class="sxs-lookup"><span data-stu-id="eccb4-110">For example, you might want your application to identify those drivers that support filters and then query each driver to determine which filter tags it supports.</span></span> <span data-ttu-id="eccb4-111">Функцию [**акмдриверенум**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) можно использовать для получения маркера для требуемого драйвера или драйверов. Этот обработчик затем можно использовать для взаимодействия с этим драйвером.</span><span class="sxs-lookup"><span data-stu-id="eccb4-111">You can use the [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) function to obtain a handle to the desired driver or drivers; this handle can then be used to communicate with that driver.</span></span>

<span data-ttu-id="eccb4-112">Обратите внимание, что когда приложение устанавливает локальный драйвер для собственного использования, функция [**акмдриверадд**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) возвращает маркер драйвера, который можно использовать для взаимодействия с драйвером.</span><span class="sxs-lookup"><span data-stu-id="eccb4-112">Note that when an application installs a local driver for its own use, the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function returns a driver handle, which can be used to communicate with the driver.</span></span> <span data-ttu-id="eccb4-113">В этом случае нет необходимости использовать **акмдриверенум** .</span><span class="sxs-lookup"><span data-stu-id="eccb4-113">It is not necessary to use **acmDriverEnum** in this case.</span></span>

 

 




