---
description: Основные понятия о разделах COM+
ms.assetid: 9fc35bef-ecc1-4764-bf69-ec89560daff4
title: Основные понятия о разделах COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 483a34e6186cda8978c1882ed1fdfbe8732f7ec8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496062"
---
# <a name="com-partitions-concepts"></a><span data-ttu-id="f5cc7-103">Основные понятия о разделах COM+</span><span class="sxs-lookup"><span data-stu-id="f5cc7-103">COM+ Partitions Concepts</span></span>

<span data-ttu-id="f5cc7-104">В вычислительных средах, где необходимо использовать разные версии или конфигурации приложения на одном компьютере, конфликты могут возникать, когда одной версии приложения требуются разные компоненты или если одной версии требуется компонент на компьютере, несовместимый с другой версией приложения.</span><span class="sxs-lookup"><span data-stu-id="f5cc7-104">In computing environments where it's necessary to use different versions or configurations of an application on the same computer, conflicts can arise when one version of the application requires different components than the other or when one version requires a component on the computer that is incompatible with the other version of the application.</span></span> <span data-ttu-id="f5cc7-105">В прошлом единственный способ решить эту проблему — поддерживать несколько компьютеров и запускать разные версии приложения на каждом компьютере.</span><span class="sxs-lookup"><span data-stu-id="f5cc7-105">In the past, the only way to solve this problem was to maintain multiple computers and run a different version of the application on each computer.</span></span> <span data-ttu-id="f5cc7-106">Такой подход является дорогостоящим и неэффективным, поскольку он увеличивает затраты на оборудование и административные издержки.</span><span class="sxs-lookup"><span data-stu-id="f5cc7-106">Such an approach is costly and inefficient because it increases hardware costs and administrative overhead.</span></span>

<span data-ttu-id="f5cc7-107">COM+ решает эту проблему, предоставляя функцию разделов COM+.</span><span class="sxs-lookup"><span data-stu-id="f5cc7-107">COM+ solves this problem by providing the COM+ partitions feature.</span></span> <span data-ttu-id="f5cc7-108">Разделы COM+ можно использовать для установки различных версий приложения COM+ на компьютере и запуска их одновременно.</span><span class="sxs-lookup"><span data-stu-id="f5cc7-108">You can use COM+ partitions to install different versions of a COM+ application on a computer and run them simultaneously.</span></span>

<span data-ttu-id="f5cc7-109">Сведения об использовании этой функции см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="f5cc7-109">To understand and use this feature, see the following topics:</span></span>

-   [<span data-ttu-id="f5cc7-110">Что такое разделы COM+?</span><span class="sxs-lookup"><span data-stu-id="f5cc7-110">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
-   [<span data-ttu-id="f5cc7-111">Реализация секционирования</span><span class="sxs-lookup"><span data-stu-id="f5cc7-111">Partition Implementation</span></span>](partition-implementation.md)
-   [<span data-ttu-id="f5cc7-112">Регистрация и Активация компонентов в секциях</span><span class="sxs-lookup"><span data-stu-id="f5cc7-112">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
-   [<span data-ttu-id="f5cc7-113">Компоненты и разделы, помещенные в очередь COM+</span><span class="sxs-lookup"><span data-stu-id="f5cc7-113">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
-   [<span data-ttu-id="f5cc7-114">Ограничения разработки приложений</span><span class="sxs-lookup"><span data-stu-id="f5cc7-114">Application Design Restrictions</span></span>](application-design-restrictions.md)

## <a name="related-topics"></a><span data-ttu-id="f5cc7-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f5cc7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5cc7-116">Задачи секций COM+</span><span class="sxs-lookup"><span data-stu-id="f5cc7-116">COM+ Partitions Tasks</span></span>](com--partitions-tasks.md)
</dt> </dl>

 

 



