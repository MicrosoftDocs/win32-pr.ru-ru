---
title: Получение сведений об ошибке расширенного RPC
description: RPC предоставляет возможность получения расширенных сведений об ошибках. В этом разделе описывается, как можно получить такую информацию об ошибке, а также приводятся рекомендации по использованию этих сведений.
ms.assetid: 7a386def-c640-42f4-9869-b6a1c522984a
keywords:
- Удаленный вызов процедур RPC, рекомендации, расширенные сведения об ошибке
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7856dd76a86763fc3f537577f9c547508fbf34ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775953"
---
# <a name="obtaining-extended-rpc-error-information"></a><span data-ttu-id="43821-105">Получение сведений об ошибке расширенного RPC</span><span class="sxs-lookup"><span data-stu-id="43821-105">Obtaining Extended RPC Error Information</span></span>

<span data-ttu-id="43821-106">RPC предоставляет возможность получения расширенных сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="43821-106">RPC provides the capability to obtain extended error information.</span></span> <span data-ttu-id="43821-107">В этом разделе описывается, как можно получить такую информацию об ошибке, а также приводятся рекомендации по использованию этих сведений.</span><span class="sxs-lookup"><span data-stu-id="43821-107">This section describes how such error information can be obtained, and offers recommendations on how to use the information.</span></span>

<span data-ttu-id="43821-108">Этот раздел разбит на следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="43821-108">This section is broken into the following topics:</span></span>

-   [<span data-ttu-id="43821-109">Необходимость в расширенных сведениях об ошибках</span><span class="sxs-lookup"><span data-stu-id="43821-109">The Need For Extended Error Information</span></span>](the-need-for-extended-error-information.md)
-   [<span data-ttu-id="43821-110">Безопасность и расширенные сведения об ошибках</span><span class="sxs-lookup"><span data-stu-id="43821-110">Security and Extended Error Information</span></span>](security-and-extended-error-information.md)
-   [<span data-ttu-id="43821-111">Включение расширенных сведений об ошибках</span><span class="sxs-lookup"><span data-stu-id="43821-111">Enabling Extended Error Information</span></span>](enabling-extended-error-information.md)
-   [<span data-ttu-id="43821-112">Основные сведения о расширенных ошибках</span><span class="sxs-lookup"><span data-stu-id="43821-112">Understanding Extended Error Information</span></span>](understanding-extended-error-information.md)
-   [<span data-ttu-id="43821-113">Надежность расширенных сведений об ошибках</span><span class="sxs-lookup"><span data-stu-id="43821-113">Reliability of Extended Error Information</span></span>](reliability-of-extended-error-information.md)
-   [<span data-ttu-id="43821-114">Независимость от других компонентов</span><span class="sxs-lookup"><span data-stu-id="43821-114">Independence From Other Components</span></span>](independence-from-other-components.md)
-   [<span data-ttu-id="43821-115">Расширенные сведения об ошибке для пользователя</span><span class="sxs-lookup"><span data-stu-id="43821-115">Extended Error Information for the User</span></span>](extended-error-information-for-the-user.md)
-   [<span data-ttu-id="43821-116">Расширенные сведения об ошибках для сервера или приложения</span><span class="sxs-lookup"><span data-stu-id="43821-116">Extended Error Information for the Server or Application</span></span>](extended-error-information-for-the-server-or-application.md)
-   [<span data-ttu-id="43821-117">Источники обнаружения расширенных сведений об ошибках</span><span class="sxs-lookup"><span data-stu-id="43821-117">Extended Error Information Detection Locations</span></span>](extended-error-information-detection-locations.md)

<span data-ttu-id="43821-118">Этот раздел тесно связан с отладкой приложений RPC.</span><span class="sxs-lookup"><span data-stu-id="43821-118">This section is closely tied with RPC application debugging.</span></span> <span data-ttu-id="43821-119">Дополнительные сведения об отладке RPC см. в разделе \[ пакет отладчика \] .</span><span class="sxs-lookup"><span data-stu-id="43821-119">For additional information about RPC debugging, see \[debugger package\].</span></span>

 

 




