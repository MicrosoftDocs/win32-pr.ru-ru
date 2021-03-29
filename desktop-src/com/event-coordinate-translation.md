---
title: Преобразование координат событий
description: Преобразование координат событий
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c40a742ead8fc8d7e431c1caa5210f0978168cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778755"
---
# <a name="event-coordinate-translation"></a><span data-ttu-id="8e6c4-103">Преобразование координат событий</span><span class="sxs-lookup"><span data-stu-id="8e6c4-103">Event Coordinate Translation</span></span>

<span data-ttu-id="8e6c4-104">Спецификация 96 для элементов управления требует, чтобы координаты, передаваемые для событий, возникающих при изменении элемента управления, HIMETRIC с точки на основе.</span><span class="sxs-lookup"><span data-stu-id="8e6c4-104">The 96 specification for controls requires that coordinates passed for events fired by the control change from being HIMETRIC to being points based.</span></span> <span data-ttu-id="8e6c4-105">Это изменение приводит к передаче событий координат в строке со свойствами и методами, поэтому преобразование координат координирует больше не несет ответственности за контейнер.</span><span class="sxs-lookup"><span data-stu-id="8e6c4-105">This change brings the event passing of coordinates in line with properties and methods and thus coordinate translation is no longer the responsibility of the container.</span></span> <span data-ttu-id="8e6c4-106">Это вызывает определенные проблемы совместимости, когда элемент управления вызывает события с помощью базы координат, которая не ожидалась, это должно быть лишь проблемой, когда в контейнере элемента управления 96 размещается старый элемент управления до 96, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="8e6c4-106">This raises certain compatibility issues where a control fires events using a coordinate base that it is not expecting, this should only be an issue where a 96 control container is hosting an older pre-96 control as follows:</span></span>

-   <span data-ttu-id="8e6c4-107">Когда в старом контейнере пред-96 размещается элемент управления 96, который элемент управления будет представлять координаты события как точки, это не должно приводить к возникновению каких-либо проблем в контейнере, так как контейнер должен распознать тип параметра.</span><span class="sxs-lookup"><span data-stu-id="8e6c4-107">When an older pre-96 container hosts a 96 control the control will present the event coordinates as points, this should not cause the container any problems as the container should recognize the parameter type.</span></span>
-   <span data-ttu-id="8e6c4-108">Если в контейнере 96 размещается элемент управления до 96, элемент управления будет представлять контейнер с координатами и будет предполагать, что в контейнере должны быть все необходимые преобразования.</span><span class="sxs-lookup"><span data-stu-id="8e6c4-108">When a 96 container hosts a pre-96 control the control will present the container with coordinates and expect the container to any translation necessary.</span></span> <span data-ttu-id="8e6c4-109">Однако контейнер 96 ожидает, что элемент управления будет соответствовать спецификации элементов управления 96 и будет представлять координаты как точки.</span><span class="sxs-lookup"><span data-stu-id="8e6c4-109">However the 96 container will be expecting a control to conform to the 96 controls specification and present its coordinates as points.</span></span> <span data-ttu-id="8e6c4-110">Элемент управления использует метод [**трансформкурдс**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) в интерфейсе [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) , предоставляемом контейнером, так же, как и для свойств и методов, чтобы добиться этого.</span><span class="sxs-lookup"><span data-stu-id="8e6c4-110">The control uses the [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) method on the [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interface provided by the container in the same way as it does for properties and methods to achieve this.</span></span>

<span data-ttu-id="8e6c4-111">В результате пользователь контейнера 96, на котором размещены элементы управления до 96, должен учитывать, что при срабатывании событий может потребоваться дальнейшее преобразование координат.</span><span class="sxs-lookup"><span data-stu-id="8e6c4-111">As a result the user of a 96 container hosting pre-96 controls will need to be aware that further translation of coordinates may be necessary when events are fired.</span></span>

 

 




