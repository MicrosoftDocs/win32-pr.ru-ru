---
description: COM+ вводит нейтральные подразделения для упрощения программирования в многопоточных средах. Нейтральный апартамент является предпочтительной моделью для COM+ для компонентов без пользовательского интерфейса.
ms.assetid: 679742af-7c04-4b0e-822a-a43e1aafa936
title: Нейтральные подразделения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac3bdff2670e4f99ad94af20278eaca6a38861e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423337"
---
# <a name="neutral-apartments"></a><span data-ttu-id="38748-104">Нейтральные подразделения</span><span class="sxs-lookup"><span data-stu-id="38748-104">Neutral Apartments</span></span>

<span data-ttu-id="38748-105">COM+ вводит нейтральные подразделения для упрощения программирования в многопоточных средах.</span><span class="sxs-lookup"><span data-stu-id="38748-105">COM+ introduces neutral apartments to simplify programming in multithreaded environments.</span></span> <span data-ttu-id="38748-106">Нейтральный апартамент является предпочтительной моделью для COM+ для компонентов без пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="38748-106">The neutral apartment is the preferred model for COM+ for components with no user interface.</span></span>

<span data-ttu-id="38748-107">В прошлом, чтобы предотвратить узкие места, Разработчики COM+, которым требуется масштабируемость сервера, приходилось реализовывать беспотоковые компоненты. Однако модели с беспроблемными потоками сложнее реализовать, поскольку они должны иметь дело с доступом через блокировку.</span><span class="sxs-lookup"><span data-stu-id="38748-107">In the past, to prevent bottlenecks, COM+ developers requiring server scalability had to implement free-threaded components; however, free-threading models are complicated to implement because they must deal with interlocking access.</span></span> <span data-ttu-id="38748-108">В нейтральных апартаментах объекты следуют рекомендациям для многопоточных подразделениях, но могут выполняться в потоках любого типа.</span><span class="sxs-lookup"><span data-stu-id="38748-108">In neutral apartments, objects follow the guidelines for multithreaded apartments but can execute on any kind of thread.</span></span> <span data-ttu-id="38748-109">Когда поток выполняется в нейтральном апартаменте, контекст объекта получается, не вызывая переключения потока.</span><span class="sxs-lookup"><span data-stu-id="38748-109">When a thread is running in a neutral apartment, the object's context is received without causing a thread switch.</span></span>

<span data-ttu-id="38748-110">Каждый процесс может иметь только один нейтральный апартамент.</span><span class="sxs-lookup"><span data-stu-id="38748-110">Each process can have only one neutral apartment.</span></span> <span data-ttu-id="38748-111">Чтобы выбрать нейтральное подразделение, используйте следующий параметр реестра:</span><span class="sxs-lookup"><span data-stu-id="38748-111">To select a neutral apartment, use the following registry setting:</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         ThreadingModel = Neutral
```

<span data-ttu-id="38748-112">Компоненты с пользовательскими интерфейсами должны по-прежнему использовать Однопотоковые подразделения в качестве предпочтительных моделей.</span><span class="sxs-lookup"><span data-stu-id="38748-112">Components that have user interfaces should continue to use single-threaded apartments as the preferred model.</span></span> <span data-ttu-id="38748-113">Чтобы выбрать однопотоковое подразделение, используйте следующий параметр реестра:</span><span class="sxs-lookup"><span data-stu-id="38748-113">To select a single-threaded apartment, use the following registry setting:</span></span>

<span data-ttu-id="38748-114">**ThreadingModel** = подразделение</span><span class="sxs-lookup"><span data-stu-id="38748-114">**ThreadingModel** = Apartment</span></span>

 

 



