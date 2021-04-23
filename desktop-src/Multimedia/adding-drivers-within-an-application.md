---
title: Добавление драйверов в приложение
description: Добавление драйверов в приложение
ms.assetid: cd9bd0a8-652b-440b-a197-81e20a9d71f1
keywords:
- Диспетчер аудиосжатия (ACM), добавление драйверов
- ACM (диспетчер аудиосжатия), добавление драйверов
- Примеры ACM, добавление драйверов
- Добавление драйверов
- Функция Акмдриверадд
- глобальные драйверы
- локальные драйверы
- Диспетчер аудиосжатия (ACM), глобальные драйверы
- ACM (диспетчер аудиосжатия), глобальные драйверы
- Диспетчер аудиосжатия (ACM), локальные драйверы
- ACM (диспетчер аудиосжатия), локальные драйверы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bf7bded89b778f271599d5ce0f8d7f7bd5f72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067990"
---
# <a name="adding-drivers-within-an-application"></a><span data-ttu-id="f201b-114">Добавление драйверов в приложение</span><span class="sxs-lookup"><span data-stu-id="f201b-114">Adding Drivers Within an Application</span></span>

<span data-ttu-id="f201b-115">Если требуется, чтобы приложение самостоятельно реализовало собственные подпрограммы сжатия, приложение может добавить драйверы в ACM, вызвав функцию [**акмдриверадд**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) .</span><span class="sxs-lookup"><span data-stu-id="f201b-115">If you need your application to implement its own compression routines internally, the application can add drivers to the ACM by calling the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function.</span></span> <span data-ttu-id="f201b-116">Приложение реализует драйвер, предоставляя функцию, которая соответствует прототипу [**акмдриверпрок**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) .</span><span class="sxs-lookup"><span data-stu-id="f201b-116">The application implements the driver by providing a function that conforms to the [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) prototype.</span></span> <span data-ttu-id="f201b-117">После добавления драйвера приложение может использовать драйвер с помощью ACM, так как он будет использовать любой другой драйвер.</span><span class="sxs-lookup"><span data-stu-id="f201b-117">After the application has added the driver, the application can use the driver through the ACM as it would use any other driver.</span></span>

<span data-ttu-id="f201b-118">ACM обрабатывает драйверы как глобальные, так и локальные.</span><span class="sxs-lookup"><span data-stu-id="f201b-118">The ACM treats drivers as either global or local.</span></span> <span data-ttu-id="f201b-119">Приложение указывает, следует ли добавлять драйвер в качестве глобального или локального при вызове **акмдриверадд**.</span><span class="sxs-lookup"><span data-stu-id="f201b-119">An application specifies whether a driver should be added as global or local when it calls **acmDriverAdd**.</span></span> <span data-ttu-id="f201b-120">Существует два различия между глобальным и локальным драйверами.</span><span class="sxs-lookup"><span data-stu-id="f201b-120">There are two differences between global and local drivers:</span></span>

-   <span data-ttu-id="f201b-121">Драйверы, добавленные в качестве глобальных драйверов, не используются совместно с другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="f201b-121">Drivers added as global drivers are not shared with other applications.</span></span>
-   <span data-ttu-id="f201b-122">Приложение может напрямую изменить приоритет глобального драйвера (но не локального драйвера), вызвав функцию [**акмдриверприорити**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) .</span><span class="sxs-lookup"><span data-stu-id="f201b-122">An application can directly alter the priority of a global driver (but not a local driver) by calling the [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) function.</span></span> <span data-ttu-id="f201b-123">ACM выполняет поиск по приоритету при поиске соответствующего драйвера для предоставления реализации вызова функции.</span><span class="sxs-lookup"><span data-stu-id="f201b-123">The ACM conducts a prioritized search when seeking an appropriate driver to provide an implementation of a function call.</span></span> <span data-ttu-id="f201b-124">ACM всегда дает локальным драйверам более высокий приоритет, чем глобальные драйверы.</span><span class="sxs-lookup"><span data-stu-id="f201b-124">The ACM always gives local drivers higher priority than global drivers.</span></span> <span data-ttu-id="f201b-125">Последний добавленный локальный драйвер имеет высший приоритет.</span><span class="sxs-lookup"><span data-stu-id="f201b-125">The most recently added local driver has highest priority.</span></span>

 

 




