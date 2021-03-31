---
description: Проектирование для развертывания
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Проектирование для развертывания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e60ac561bd05d08253433e52c7f00c2def54df3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496038"
---
# <a name="designing-for-deployment"></a><span data-ttu-id="91cb0-103">Проектирование для развертывания</span><span class="sxs-lookup"><span data-stu-id="91cb0-103">Designing for Deployment</span></span>

<span data-ttu-id="91cb0-104">Планирование области применения приложений COM+ — важная задача разработки, которую следует рассмотреть на раннем этапе.</span><span class="sxs-lookup"><span data-stu-id="91cb0-104">Planning the scope of COM+ applications is an important design task you should consider early on.</span></span> <span data-ttu-id="91cb0-105">Распределенные системы, предназначенные для запуска с помощью COM+, должны быть разработаны для развертывания с минимальным объемом индивидуальной конфигурации и наиболее эффективно использовать каждый процесс.</span><span class="sxs-lookup"><span data-stu-id="91cb0-105">Distributed systems that are intended to run using COM+ should be designed for deployment with the least amount of individual configuration and to most efficiently use each process.</span></span> <span data-ttu-id="91cb0-106">Существуют также методы, которые позволяют добиться оптимальной производительности при развертывании приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="91cb0-106">There are also techniques you can use that will enable you to achieve optimal performance when deploying a COM+ application.</span></span> <span data-ttu-id="91cb0-107">(Дополнительные сведения см. в разделе [развертывание для ускорения обмена данными](deploying-for-faster-communication.md).)</span><span class="sxs-lookup"><span data-stu-id="91cb0-107">(For more information, see [Deploying for Faster Communication](deploying-for-faster-communication.md).)</span></span>

<span data-ttu-id="91cb0-108">При просмотре с помощью средства администрирования "службы компонентов" каждое приложение COM+ отображается в виде папки, в которой Наборы компонентов логически группируются.</span><span class="sxs-lookup"><span data-stu-id="91cb0-108">When viewed with the Component Services administrative tool, each COM+ application appears as a folder within which sets of components are logically grouped.</span></span> <span data-ttu-id="91cb0-109">Хотя отдельные компоненты можно перемещать между папками **компонентов** приложения COM+ (иными словами, из одного приложения в другое), некоторые службы, установленные на уровне приложения COM+, такие как безопасность, могут различаться.</span><span class="sxs-lookup"><span data-stu-id="91cb0-109">While you can move individual components between COM+ application **Components** folders (in other words, from one application to another), several services set at the COM+ application level, such as security, may differ.</span></span> <span data-ttu-id="91cb0-110">Эти параметры службы могут повлиять на переносимость.</span><span class="sxs-lookup"><span data-stu-id="91cb0-110">These service settings can affect portability.</span></span>

## <a name="a-com-server-application-defines-a-process-boundary"></a><span data-ttu-id="91cb0-111">Серверное приложение COM+ определяет границу процесса</span><span class="sxs-lookup"><span data-stu-id="91cb0-111">A COM+ Server Application Defines a Process Boundary</span></span>

<span data-ttu-id="91cb0-112">При создании нового серверного приложения COM+ вы фактически определяете новую границу процесса.</span><span class="sxs-lookup"><span data-stu-id="91cb0-112">When you create a new COM+ server application, you are really defining a new process boundary.</span></span> <span data-ttu-id="91cb0-113">(Обратите внимание на исключение для библиотечных приложений, описанных ниже.) Этот процесс превращается в Управляющий экземпляр приложения для компонентов, содержащихся в приложении COM+.</span><span class="sxs-lookup"><span data-stu-id="91cb0-113">(Note the exception for library applications explained below.) This process becomes the controlling application instance for the components that are contained in the COM+ application.</span></span> <span data-ttu-id="91cb0-114">Все эти компоненты выполняются в процессе в новом экземпляре исполняемой программы COM+ каждый раз, когда программа вызывает приложение COM+ в первый раз.</span><span class="sxs-lookup"><span data-stu-id="91cb0-114">These components all run in-process in a new instance of the COM+ executable program whenever a program calls into a COM+ application for the first time.</span></span> <span data-ttu-id="91cb0-115">Это означает, что все компоненты в заданной папке **Components** приложения COM+ выполняются в одном пространстве процесса, который выступает в качестве сервера DCOM.</span><span class="sxs-lookup"><span data-stu-id="91cb0-115">This means that all of the components within a given COM+ application's **Components** folder run in a single process space that serves as the DCOM server.</span></span> <span data-ttu-id="91cb0-116">В приложении COM+ COM+ управляет памятью, координации с координатор распределенных транзакций (DTC), JIT-активацией экземпляра компонента, обнаружением и восстановлением сбоев, а также безопасностью на основе ролей.</span><span class="sxs-lookup"><span data-stu-id="91cb0-116">Within the COM+ application, COM+ manages memory, coordination with the Distributed Transaction Coordinator (DTC), just-in-time component instance activation, crash detection and recovery, and role-based security.</span></span>

## <a name="calling-across-com-application-boundaries"></a><span data-ttu-id="91cb0-117">Вызов через границы приложения COM+</span><span class="sxs-lookup"><span data-stu-id="91cb0-117">Calling Across COM+ Application Boundaries</span></span>

<span data-ttu-id="91cb0-118">Поскольку каждое приложение COM+ обычно реализуется как отдельный исполняемый файл, результат разбиения распределенного приложения по нескольким приложениям COM+ вводит необработанные вызовы COM, когда компоненты в одном приложении COM+ вызывают компоненты в другом приложении COM+.</span><span class="sxs-lookup"><span data-stu-id="91cb0-118">Because each COM+ application normally is implemented as a separate executable, the effect of splitting a distributed application across multiple COM+ applications introduces out-of-process COM calls when components in one COM+ application call the components in another COM+ application.</span></span> <span data-ttu-id="91cb0-119">Это приводит к снижению производительности из-за дополнительных затрат на упаковку параметров COM между процессами.</span><span class="sxs-lookup"><span data-stu-id="91cb0-119">This introduces performance degradation due to the extra burden that marshaling COM parameters across processes imposes.</span></span>

> [!Note]  
> <span data-ttu-id="91cb0-120">Нет ничего плохого в возникновении этого снижения производительности. нужно только знать, что он будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="91cb0-120">There is nothing inherently wrong with incurring this performance penalty; you just need to be aware that it is going to occur.</span></span> <span data-ttu-id="91cb0-121">В зависимости от требуемого времени ответа число пользователей, которые будут одновременно запрашивать бизнес-услуги, а также дополнительную нагрузку, которая добавляется каждым компонентом в каждое приложение COM+, может оказаться, что производительность, доступная для межприложенийных вызовов, приемлема.</span><span class="sxs-lookup"><span data-stu-id="91cb0-121">Depending on the required response time, the number of users that will simultaneously request business services, and the added start-up burden that each component adds to each COM+ application, you may find that the performance hit attributable to cross-application calls is acceptable.</span></span>

 

<span data-ttu-id="91cb0-122">Одна из возможных сторон, которая устраняет снижение производительности при вызове через границы приложения COM+, заключается в пометке приложения COM+ как приложения библиотеки.</span><span class="sxs-lookup"><span data-stu-id="91cb0-122">One possibility that eliminates the performance penalty of calling across COM+ application boundaries is to mark a given COM+ application as a library application.</span></span> <span data-ttu-id="91cb0-123">Приложение библиотеки COM+ выполняется в процессе клиента, который его создает.</span><span class="sxs-lookup"><span data-stu-id="91cb0-123">A COM+ library application runs in the process of the client that creates it.</span></span> <span data-ttu-id="91cb0-124">Конечно, отсутствие затрат на повышение производительности не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="91cb0-124">Of course, no performance gain has zero cost.</span></span> <span data-ttu-id="91cb0-125">В этом случае компромисс включает ограничения приложений библиотеки COM+.</span><span class="sxs-lookup"><span data-stu-id="91cb0-125">In this case, the trade-off involves the limitations of COM+ library applications.</span></span> <span data-ttu-id="91cb0-126">Приложение библиотеки может использовать безопасность на основе ролей, но не может поддерживать компоненты очередей или удаленный доступ.</span><span class="sxs-lookup"><span data-stu-id="91cb0-126">While a library application can use role-based security, it cannot support queued components or remote access.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91cb0-127">См. также</span><span class="sxs-lookup"><span data-stu-id="91cb0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91cb0-128">Развертывание для ускорения обмена данными</span><span class="sxs-lookup"><span data-stu-id="91cb0-128">Deploying for Faster Communication</span></span>](deploying-for-faster-communication.md)
</dt> <dt>

[<span data-ttu-id="91cb0-129">Проектирование для обеспечения доступности</span><span class="sxs-lookup"><span data-stu-id="91cb0-129">Designing for Availability</span></span>](designing-for-availability.md)
</dt> <dt>

[<span data-ttu-id="91cb0-130">Проектирование для масштабируемости</span><span class="sxs-lookup"><span data-stu-id="91cb0-130">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="91cb0-131">Разработка для обеспечения безопасности</span><span class="sxs-lookup"><span data-stu-id="91cb0-131">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



