---
title: Состояние постоянного объекта
description: Состояние постоянного объекта
ms.assetid: 731fef03-d204-48e7-b33a-801e97a9d2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c08d4dd1175b5a7681f79fa9049772af245a031
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328979"
---
# <a name="persistent-object-state"></a><span data-ttu-id="7c7a3-103">Состояние постоянного объекта</span><span class="sxs-lookup"><span data-stu-id="7c7a3-103">Persistent Object State</span></span>

<span data-ttu-id="7c7a3-104">Некоторые COM-объекты могут сохранять свое внутреннее состояние при запросе клиента.</span><span class="sxs-lookup"><span data-stu-id="7c7a3-104">Some COM objects can save their internal state when asked to do so by a client.</span></span>

<span data-ttu-id="7c7a3-105">COM определяет стандарты, с помощью которых клиенты могут запрашивать инициализацию, загрузку и сохранение объектов в хранилище данных (например, неструктурированный файл, структурированное хранилище или память).</span><span class="sxs-lookup"><span data-stu-id="7c7a3-105">COM defines standards through which clients can request objects to be initialized, loaded, and saved to and from a data store (for example, flat file, structured storage, or memory).</span></span> <span data-ttu-id="7c7a3-106">Ответственность за управление расположением, в котором хранятся сохраняемые данные объекта, является обязанностью клиента, но не формат данных.</span><span class="sxs-lookup"><span data-stu-id="7c7a3-106">It is the client's responsibility to manage the location where the object's persistent data is stored but not the format of the data.</span></span> <span data-ttu-id="7c7a3-107">Объекты COM, которые соответствуют этим стандартам, называются *постоянными объектами*.</span><span class="sxs-lookup"><span data-stu-id="7c7a3-107">COM objects that adhere to these standards are called *persistent objects*.</span></span>

<span data-ttu-id="7c7a3-108">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="7c7a3-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="7c7a3-109">Постоянные интерфейсы объектов</span><span class="sxs-lookup"><span data-stu-id="7c7a3-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
-   [<span data-ttu-id="7c7a3-110">Инициализация постоянных объектов</span><span class="sxs-lookup"><span data-stu-id="7c7a3-110">Initializing Persistent Objects</span></span>](initializing-persistent-objects.md)

## <a name="related-topics"></a><span data-ttu-id="7c7a3-111">См. также</span><span class="sxs-lookup"><span data-stu-id="7c7a3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c7a3-112">COM-клиенты и серверы</span><span class="sxs-lookup"><span data-stu-id="7c7a3-112">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




