---
title: Вход в состояние выполнения
description: Вход в состояние выполнения
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959038c8f64fe8750ab1bcf0f06b753371f04136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986415"
---
# <a name="entering-the-running-state"></a><span data-ttu-id="2e223-103">Вход в состояние выполнения</span><span class="sxs-lookup"><span data-stu-id="2e223-103">Entering the Running State</span></span>

<span data-ttu-id="2e223-104">Когда внедренный объект выполняет переход в состояние выполнения, обработчик объектов должен нахождение и запуск серверного приложения для использования служб, которые предоставляет только сервер.</span><span class="sxs-lookup"><span data-stu-id="2e223-104">When an embedded object makes the transition to the running state, the object handler must locate and run the server application in order to utilize the services that only the server provides.</span></span> <span data-ttu-id="2e223-105">Внедренные объекты помещаются в состояние выполнения явным образом через запрос контейнера, например, необходимо нарисовать формат, который в данный момент не был кэширован, или неявно OLE в ответ на вызов некоторой операции, например, когда пользователь контейнера дважды щелкает объект.</span><span class="sxs-lookup"><span data-stu-id="2e223-105">Embedded objects are placed in the running state either explicitly through a request by the container, such as a need to draw a format not currently cached, or implicitly by OLE in response to invoking some operation, such as when a user of the container double-clicks the object.</span></span>

<span data-ttu-id="2e223-106">Когда связанный объект выполняет переход в состояние выполнения, процесс называется *привязкой*.</span><span class="sxs-lookup"><span data-stu-id="2e223-106">When a linked object makes the transition into the running state, the process is known as *binding*.</span></span> <span data-ttu-id="2e223-107">В процессе привязки обработчик объектов запрашивает сохраненное моникер для размещения данных ссылки, а затем запускает серверное приложение.</span><span class="sxs-lookup"><span data-stu-id="2e223-107">In the process of binding, the object handler asks its stored moniker to locate the link's data, then runs the server application.</span></span>

<span data-ttu-id="2e223-108">На первый взгляд, привязка связанного объекта не сложнее, чем выполнение внедренного объекта.</span><span class="sxs-lookup"><span data-stu-id="2e223-108">At first glance, binding a linked object appears to be no more complicated than running an embedded object.</span></span> <span data-ttu-id="2e223-109">Однако следующие моменты усложняют процесс:</span><span class="sxs-lookup"><span data-stu-id="2e223-109">However, the following points complicate the process:</span></span>

-   <span data-ttu-id="2e223-110">Ссылка может ссылаться на объект или часть, которая внедрена в другой контейнер.</span><span class="sxs-lookup"><span data-stu-id="2e223-110">A link can refer to an object, or a portion thereof, that is embedded in another container.</span></span> <span data-ttu-id="2e223-111">Эта возможность подразумевает возможность вложенных внедрений.</span><span class="sxs-lookup"><span data-stu-id="2e223-111">This capability implies a potential for nested embeddings.</span></span> <span data-ttu-id="2e223-112">Разрешение ссылок на такую иерархию требует рекурсивного прохода по *составному моникеру*, начиная с крайнего правого элемента.</span><span class="sxs-lookup"><span data-stu-id="2e223-112">Resolving references to such a hierarchy requires recursively traversing a *composite moniker*, beginning with the rightmost member.</span></span>
-   <span data-ttu-id="2e223-113">Когда источник связи выполняется, OLE привязывается к выполняющемуся экземпляру объекта, а не к другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="2e223-113">When the link source is running, OLE binds to the running instance of the object rather than running another instance.</span></span> <span data-ttu-id="2e223-114">В случае вложенных внедренных объектов, один из которых является источником ссылки, OLE должен иметь возможность привязки к уже выполняющемуся объекту в любой точке.</span><span class="sxs-lookup"><span data-stu-id="2e223-114">In the case of nested embedded objects, one of which is the link source, OLE must be able to bind to an already running object at any point.</span></span>
-   <span data-ttu-id="2e223-115">Для выполнения объекта требуется доступ к области хранения для объекта.</span><span class="sxs-lookup"><span data-stu-id="2e223-115">Running an object requires accessing the storage area for the object.</span></span> <span data-ttu-id="2e223-116">При запуске внедренного объекта OLE получает указатель на хранилище во время процесса загрузки, который передается в приложение OLE-сервера.</span><span class="sxs-lookup"><span data-stu-id="2e223-116">When an embedded object is run, OLE receives a pointer to the storage during the load process, which it passes on to the OLE server application.</span></span> <span data-ttu-id="2e223-117">Однако для связанных объектов нет стандартного интерфейса для доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="2e223-117">For linked objects, however, there is no standard interface for accessing storage.</span></span> <span data-ttu-id="2e223-118">Серверное приложение OLE может использовать интерфейс файловой системы или другой механизм.</span><span class="sxs-lookup"><span data-stu-id="2e223-118">The OLE server application may use the file system interface or some other mechanism.</span></span>

 

 




