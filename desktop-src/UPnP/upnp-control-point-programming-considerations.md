---
title: Вопросы программирования контрольной точки
description: Разработчики, создающие приложения на основе UPnP (или контрольные точки), должны использовать эти приложения из \_ клиента апартментсреадед. Существуют известные проблемы при использовании API управляющей точки из \_ многопоточного клиента, выполняющегося под нагрузкой.
ms.assetid: a5d79a29-4192-40af-b75d-a31f1f46149c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76955177f9fc0c3b164d84998547c1afdfbfb4bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888900"
---
# <a name="control-point-programming-considerations"></a><span data-ttu-id="a8f51-104">Вопросы программирования контрольной точки</span><span class="sxs-lookup"><span data-stu-id="a8f51-104">Control Point Programming Considerations</span></span>

<span data-ttu-id="a8f51-105">Разработчики, создающие приложения на основе UPnP (или контрольные точки), должны использовать эти приложения из \_ клиента апартментсреадед.</span><span class="sxs-lookup"><span data-stu-id="a8f51-105">Developers who create UPnP-based applications (or control points) must use these applications from a COINIT\_APARTMENTTHREADED client.</span></span> <span data-ttu-id="a8f51-106">Существуют известные проблемы при использовании API управляющей точки из \_ многопоточного клиента, выполняющегося под нагрузкой.</span><span class="sxs-lookup"><span data-stu-id="a8f51-106">There are known problems when using the Control Point API from a COINIT\_MULTITHREADED client running under stress.</span></span>

 

 




