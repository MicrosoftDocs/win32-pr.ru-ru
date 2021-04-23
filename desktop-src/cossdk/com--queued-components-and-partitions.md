---
description: Служба COM+ в очереди компонентов полностью поддерживает понятие секций. Это значит, что при выполнении компонента, помещенного в очередь в пределах секции, сообщение помещается в очередь и компонент в конечном итоге выполняется в разделе Components.
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: Компоненты и разделы, помещенные в очередь COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589d7cb7c3e61be8ef53a248f990cde65447cf9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538615"
---
# <a name="com-queued-components-and-partitions"></a><span data-ttu-id="725a6-104">Компоненты и разделы, помещенные в очередь COM+</span><span class="sxs-lookup"><span data-stu-id="725a6-104">COM+ Queued Components and Partitions</span></span>

<span data-ttu-id="725a6-105">Служба COM+ в очереди компонентов полностью поддерживает понятие секций.</span><span class="sxs-lookup"><span data-stu-id="725a6-105">The COM+ queued components service fully supports the concept of partitions.</span></span> <span data-ttu-id="725a6-106">Это значит, что при выполнении компонента, помещенного в очередь в секции, сообщение помещается в очередь и компонент в конечном итоге выполняется в секции компонента.</span><span class="sxs-lookup"><span data-stu-id="725a6-106">That is, when a queued component within a partition is executed, the message is queued and the component is eventually executed within the component's partition.</span></span>

## <a name="queue-names-for-partitioned-components"></a><span data-ttu-id="725a6-107">Имена очередей для секционированных компонентов</span><span class="sxs-lookup"><span data-stu-id="725a6-107">Queue Names for Partitioned Components</span></span>

<span data-ttu-id="725a6-108">Обычно служба очередей компонентов использует имя приложения в качестве имени очереди.</span><span class="sxs-lookup"><span data-stu-id="725a6-108">Traditionally, the queued components service uses the application name as the queue name.</span></span> <span data-ttu-id="725a6-109">Это означает, что в сценарии, не относящемся к секциям, где на компьютере существует только один экземпляр имени приложения, каждое имя приложения имеет собственную очередь сообщений.</span><span class="sxs-lookup"><span data-stu-id="725a6-109">This means that in a non-partitions scenario, where only one instance of an application name exists on a computer, each application name has its own message queue.</span></span>

<span data-ttu-id="725a6-110">Однако в случае секций, где на компьютере может существовать несколько экземпляров одного и того же имени приложения, служба очередей компонентов использует одну и ту же очередь для всех компонентов, использующих одно и то же имя приложения.</span><span class="sxs-lookup"><span data-stu-id="725a6-110">In the case of partitions, however, where multiple instances of the same application name can exist on a computer, the queued components service uses the same queue for any queued components that share the same application name.</span></span>

## <a name="activating-queued-components"></a><span data-ttu-id="725a6-111">Активация компонентов в очереди</span><span class="sxs-lookup"><span data-stu-id="725a6-111">Activating Queued Components</span></span>

<span data-ttu-id="725a6-112">Те же правила, с помощью которых идентификатор секции используется для активации компонента, не относящегося к очереди, применяются к компоненту, расположенному в очереди, следующим образом.</span><span class="sxs-lookup"><span data-stu-id="725a6-112">The same rules for how the partition ID is used to activate a non-queued component applies to a queued component, as follows:</span></span>

-   <span data-ttu-id="725a6-113">Если моникер используется для активации компонента в очереди и включен идентификатор секции, этот идентификатор секции используется для нахождение секции.</span><span class="sxs-lookup"><span data-stu-id="725a6-113">If a moniker is used to activate the queued component and a partition ID is included, this partition ID is used to locate the partition.</span></span> <span data-ttu-id="725a6-114">Этот идентификатор секции имеет приоритет над любым ИДЕНТИФИКАТОРом секции, который может существовать в контексте активируемого компонента.</span><span class="sxs-lookup"><span data-stu-id="725a6-114">This partition ID takes precedence over any partition ID that might exist in the context for the component being activated.</span></span>
-   <span data-ttu-id="725a6-115">Если моникер не используется для активации компонента, используется идентификатор раздела, который находится в контексте объекта.</span><span class="sxs-lookup"><span data-stu-id="725a6-115">If no moniker is being used to activate the component, the partition ID that is in the object's context is used.</span></span>
-   <span data-ttu-id="725a6-116">Если в контексте объекта не существует идентификатора секции, используется сопоставление пользователя с Секцией по умолчанию в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="725a6-116">If no partition ID exists in the object's context, the default user-to-partition mapping within Active Directory is used.</span></span>

> [!Note]  
> <span data-ttu-id="725a6-117">Если серверный компьютер отключается от сети, а сопоставление набора разделов «пользователь-Секция» изменяется в то время, когда сервер отключен, то кэш разделов может содержать устаревшее сопоставление набора разделов «пользователь-секция».</span><span class="sxs-lookup"><span data-stu-id="725a6-117">If a server computer is disconnected from the network and if the user-to-partition set mapping is changed while the server is disconnected, the partition cache might contain outdated user-to-partition set mapping.</span></span> <span data-ttu-id="725a6-118">Это может привести к ошибке активации, если сопоставление пользовательских наборов секций является механизмом, используемым для активации компонента.</span><span class="sxs-lookup"><span data-stu-id="725a6-118">This could result in an activation error if user-to-partition set mapping is the mechanism used to activate a component.</span></span>

 

<span data-ttu-id="725a6-119">События COM+ полностью интегрированы в разделы.</span><span class="sxs-lookup"><span data-stu-id="725a6-119">COM+ events are fully integrated into partitions.</span></span> <span data-ttu-id="725a6-120">Это означает, что подписчик может подписываться на издателя, чье приложение находится в пределах секции.</span><span class="sxs-lookup"><span data-stu-id="725a6-120">This means that a subscriber can subscribe to a publisher whose application resides within a partition.</span></span> <span data-ttu-id="725a6-121">Чтобы разрешить эту подписку, коллекция классов подписчика включает два свойства, связанные с Секцией — идентификатор секции класса событий и идентификатор приложения класса событий.</span><span class="sxs-lookup"><span data-stu-id="725a6-121">To allow this subscription, the subscriber class collection includes two partition-related properties—an event class partition ID and an event class application ID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="725a6-122">См. также</span><span class="sxs-lookup"><span data-stu-id="725a6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="725a6-123">Ограничения разработки приложений</span><span class="sxs-lookup"><span data-stu-id="725a6-123">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="725a6-124">Реализация секционирования</span><span class="sxs-lookup"><span data-stu-id="725a6-124">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="725a6-125">Регистрация и Активация компонентов в секциях</span><span class="sxs-lookup"><span data-stu-id="725a6-125">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="725a6-126">Что такое разделы COM+?</span><span class="sxs-lookup"><span data-stu-id="725a6-126">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



