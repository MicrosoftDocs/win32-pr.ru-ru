---
description: Регистрация и Активация компонентов в секциях
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Регистрация и Активация компонентов в секциях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31790bc9a3df12d961a4b16271937ae22f963c38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538801"
---
# <a name="registering-and-activating-components-in-partitions"></a><span data-ttu-id="e8f39-103">Регистрация и Активация компонентов в секциях</span><span class="sxs-lookup"><span data-stu-id="e8f39-103">Registering and Activating Components in Partitions</span></span>

<span data-ttu-id="e8f39-104">После создания раздела на следующем шаге выполняется регистрация компонентов COM+ в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="e8f39-104">After a partition has been created, the next step is register your COM+ components within that partition.</span></span> <span data-ttu-id="e8f39-105">Компонент регистрируется в разделе при создании нового приложения COM+ или при установке существующего приложения COM+ в раздел.</span><span class="sxs-lookup"><span data-stu-id="e8f39-105">A component is registered within a partition when a new COM+ application is created or when an existing COM+ application is installed into the partition.</span></span> <span data-ttu-id="e8f39-106">Чтобы упростить администрирование регистрации, когда несколько секций содержат одинаковые компоненты COM+, служба partitions позволяет администратору копировать приложения или компоненты из одной секции в другую.</span><span class="sxs-lookup"><span data-stu-id="e8f39-106">To ease the administration of registration when multiple partitions contain the same COM+ components, the partitions service allows an administrator to copy applications or components from one partition into another.</span></span> <span data-ttu-id="e8f39-107">При копировании приложения или компонента COM+ все связанные с ним свойства разделов копируются вместе с удостоверением приложения или любым из членов роли.</span><span class="sxs-lookup"><span data-stu-id="e8f39-107">When a COM+ application or a component is copied, all associated partition properties are copied with it, except the application's identity or any of the members of a role.</span></span>

<span data-ttu-id="e8f39-108">Когда клиентская программа вызывает функцию [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) или [**кожетобжект**](/windows/desktop/api/objbase/nf-objbase-cogetobject) для создания экземпляра объекта, com+ выполняет два отдельных шага, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="e8f39-108">When the client program calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) function to instantiate an object, COM+ performs two distinct steps, as follows:</span></span>

1.  <span data-ttu-id="e8f39-109">Находит секцию, в которой находится компонент</span><span class="sxs-lookup"><span data-stu-id="e8f39-109">Locates the partition in which the component resides</span></span>
2.  <span data-ttu-id="e8f39-110">Находит нужный компонент в этой секции</span><span class="sxs-lookup"><span data-stu-id="e8f39-110">Locates the correct component within that partition</span></span>

<span data-ttu-id="e8f39-111">Эти действия подробно описаны в следующих подразделах этого раздела:</span><span class="sxs-lookup"><span data-stu-id="e8f39-111">The following topics in this section describe these steps in detail:</span></span>

-   [<span data-ttu-id="e8f39-112">Поиск секций во время активации</span><span class="sxs-lookup"><span data-stu-id="e8f39-112">Locating Partitions During Activation</span></span>](locating-partitions-during-activation.md)
-   [<span data-ttu-id="e8f39-113">Поиск компонента для активации</span><span class="sxs-lookup"><span data-stu-id="e8f39-113">Locating a Component for Activation</span></span>](locating-a-component-for-activation.md)

## <a name="related-topics"></a><span data-ttu-id="e8f39-114">См. также</span><span class="sxs-lookup"><span data-stu-id="e8f39-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8f39-115">Ограничения разработки приложений</span><span class="sxs-lookup"><span data-stu-id="e8f39-115">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="e8f39-116">Компоненты и разделы, помещенные в очередь COM+</span><span class="sxs-lookup"><span data-stu-id="e8f39-116">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="e8f39-117">Реализация секционирования</span><span class="sxs-lookup"><span data-stu-id="e8f39-117">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="e8f39-118">Что такое разделы COM+?</span><span class="sxs-lookup"><span data-stu-id="e8f39-118">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 
