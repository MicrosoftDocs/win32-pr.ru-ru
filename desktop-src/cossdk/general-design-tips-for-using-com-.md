---
description: Ключевым для хорошего проектирования является планирование. Если вы не знакомы с проектированием трехуровневого приложения, см. раздел, посвященный проектированию приложения COM+ с помощью UML.
ms.assetid: 463f4154-92f6-46c3-95ff-8513963dcadd
title: Общие рекомендации по проектированию для использования COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5765259f170b1a98f1abb2d097dfdaec2e09d47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141375"
---
# <a name="general-design-tips-for-using-com"></a><span data-ttu-id="01f2f-104">Общие рекомендации по проектированию для использования COM+</span><span class="sxs-lookup"><span data-stu-id="01f2f-104">General Design Tips for Using COM+</span></span>

<span data-ttu-id="01f2f-105">Ключевым для хорошего проектирования является планирование.</span><span class="sxs-lookup"><span data-stu-id="01f2f-105">The key to good design is planning.</span></span> <span data-ttu-id="01f2f-106">Если вы не знакомы с проектированием трехуровневого приложения, см. раздел, посвященный [проектированию приложения COM+ с помощью UML](designing-the-com--application-using-uml.md).</span><span class="sxs-lookup"><span data-stu-id="01f2f-106">If you are unfamiliar with designing a three-tier application, see the section entitled [Designing the COM+ Application Using UML](designing-the-com--application-using-uml.md).</span></span>

<span data-ttu-id="01f2f-107">Создание компонентов COM, составляющих средний уровень приложения COM+, может существенно повлиять на производительность, масштабируемость и простоту развертывания.</span><span class="sxs-lookup"><span data-stu-id="01f2f-107">How you construct the COM components that make up the middle tier of your COM+ application can dramatically affect performance, scalability, and ease of deployment.</span></span> <span data-ttu-id="01f2f-108">В следующих разделах приводятся рекомендации по проектированию и рекомендации по реализации, о которых следует знать при проектировании COM-компонентов.</span><span class="sxs-lookup"><span data-stu-id="01f2f-108">The following topics provide design considerations and implementation tips you should know about when designing COM components.</span></span>



| <span data-ttu-id="01f2f-109">Раздел</span><span class="sxs-lookup"><span data-stu-id="01f2f-109">Topic</span></span>                                                                   | <span data-ttu-id="01f2f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="01f2f-110">Description</span></span>                                                                                                                |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01f2f-111">Проектирование для масштабируемости</span><span class="sxs-lookup"><span data-stu-id="01f2f-111">Designing for Scalability</span></span>](designing-for-scalability.md)<br/>   | <span data-ttu-id="01f2f-112">Предлагает способы повышения масштабируемости приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="01f2f-112">Suggests ways to increase the scalability of your COM+ application.</span></span><br/>                                             |
| [<span data-ttu-id="01f2f-113">Проектирование для обеспечения доступности</span><span class="sxs-lookup"><span data-stu-id="01f2f-113">Designing for Availability</span></span>](designing-for-availability.md)<br/> | <span data-ttu-id="01f2f-114">Обсуждаются службы, которые можно использовать для повышения доступности функций среднего уровня в приложениях COM+.</span><span class="sxs-lookup"><span data-stu-id="01f2f-114">Discusses services you can use to improve the availability your middle-tier functionality in COM+ applications.</span></span><br/> |
| [<span data-ttu-id="01f2f-115">Разработка для обеспечения безопасности</span><span class="sxs-lookup"><span data-stu-id="01f2f-115">Designing for Security</span></span>](designing-for-security.md)<br/>         | <span data-ttu-id="01f2f-116">Описывает способы наиболее эффективного настройки безопасности для приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="01f2f-116">Discusses ways to most efficiently set up security for a COM+ application.</span></span><br/>                                      |
| [<span data-ttu-id="01f2f-117">Проектирование для развертывания</span><span class="sxs-lookup"><span data-stu-id="01f2f-117">Designing for Deployment</span></span>](designing-for-deployment.md)<br/>     | <span data-ttu-id="01f2f-118">Описывает способы снижения проблем развертывания при проектировании распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="01f2f-118">Discusses ways to minimize deployment headaches when designing a distributed application.</span></span><br/>                       |



 

<span data-ttu-id="01f2f-119">Кроме того, не забудьте [повысить производительность с помощью пула объектов](improving-performance-with-object-pooling.md) для наиболее эффективного использования пула объектов.</span><span class="sxs-lookup"><span data-stu-id="01f2f-119">Also, be sure to see [Improving Performance with Object Pooling](improving-performance-with-object-pooling.md) for ways to most effectively use object pooling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01f2f-120">См. также</span><span class="sxs-lookup"><span data-stu-id="01f2f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01f2f-121">Предположения и принципы разработки COM+</span><span class="sxs-lookup"><span data-stu-id="01f2f-121">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="01f2f-122">Проектирование приложения COM+ с помощью UML</span><span class="sxs-lookup"><span data-stu-id="01f2f-122">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="01f2f-123">Оптимизация взаимодействия с уровнем бизнес-логики COM+</span><span class="sxs-lookup"><span data-stu-id="01f2f-123">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="01f2f-124">Другие средства Майкрософт для создания распределенных приложений</span><span class="sxs-lookup"><span data-stu-id="01f2f-124">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 




