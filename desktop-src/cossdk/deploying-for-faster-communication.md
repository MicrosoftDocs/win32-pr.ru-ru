---
description: Развертывание для ускорения обмена данными
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Развертывание для ускорения обмена данными
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2594a7dbd34813013257350e2deb9d93db6bae5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673150"
---
# <a name="deploying-for-faster-communication"></a><span data-ttu-id="111b1-103">Развертывание для ускорения обмена данными</span><span class="sxs-lookup"><span data-stu-id="111b1-103">Deploying for Faster Communication</span></span>

<span data-ttu-id="111b1-104">Производительность является ключевым фактором при развертывании приложения COM+, а расположение компонента является ключом к повышению производительности от хорошо спроектированного приложения.</span><span class="sxs-lookup"><span data-stu-id="111b1-104">Performance is a key consideration when deploying a COM+ application, and component location is the key to getting the best performance from a well-designed application.</span></span>

<span data-ttu-id="111b1-105">Это было однажды, что при масштабируемой архитектуре приложений производительность может быть решена путем простого перемещения основных компонентов приложения на более производительное оборудование.</span><span class="sxs-lookup"><span data-stu-id="111b1-105">It was once widely held that with scalable application architectures, performance could be addressed by simply moving primary components of the application to faster hardware.</span></span> <span data-ttu-id="111b1-106">Это было признано недействительным.</span><span class="sxs-lookup"><span data-stu-id="111b1-106">This has proven not to be true.</span></span> <span data-ttu-id="111b1-107">Проблемы с производительностью возникают не из – за производительности отдельных компонентов, а из ссылок, соединяющих компоненты.</span><span class="sxs-lookup"><span data-stu-id="111b1-107">Performance problems arise not from individual component performance but from the links connecting components.</span></span>

<span data-ttu-id="111b1-108">Основным фактором успеха является расположение.</span><span class="sxs-lookup"><span data-stu-id="111b1-108">The primary factor for success is location.</span></span> <span data-ttu-id="111b1-109">Близость или физическое расположение, время, емкость и назначение — это отдельные аспекты расположения, которые применяются к развертыванию приложения COM+, что влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="111b1-109">Proximity or physical location, time, capacity, and purpose are distinct aspects of location that apply to the deployment of a COM+ application, all of which affect performance.</span></span>

<span data-ttu-id="111b1-110">Оптимальная производительность возникает, когда компоненты и ресурсы приложения разрабатываются и развертываются в соответствии с потребностями, установленными в рабочей нагрузке приложения.</span><span class="sxs-lookup"><span data-stu-id="111b1-110">The best performance comes when the application components and resources are designed and deployed to match the demands placed upon them by the application workload.</span></span>

<span data-ttu-id="111b1-111">В общем случае следует развертывать компоненты для сворачивания межпроцессного и, в частности, межкомпьютерного взаимодействия между компонентами.</span><span class="sxs-lookup"><span data-stu-id="111b1-111">In general, you should deploy components to minimize cross-process, and especially cross-computer, communication between components.</span></span> <span data-ttu-id="111b1-112">Если структура приложения является эффективной, то классы внутри компонента группируются по функциям и используются для максимального увеличения взаимодействия между компонентами.</span><span class="sxs-lookup"><span data-stu-id="111b1-112">If your application design is efficient, classes within a component are grouped by use and function to maximize communications within components.</span></span> <span data-ttu-id="111b1-113">При развертывании компонентов необходимо убедиться, что компоненты логически расположены, чтобы использовать связи между компонентами и уменьшить объем обмена сообщениями между компонентами.</span><span class="sxs-lookup"><span data-stu-id="111b1-113">In deploying components, you need to ensure that the components are logically located to make use of the relationships between the components and to reduce the amount of messaging between components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="111b1-114">См. также</span><span class="sxs-lookup"><span data-stu-id="111b1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="111b1-115">Проектирование для развертывания</span><span class="sxs-lookup"><span data-stu-id="111b1-115">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> </dl>

 

 



