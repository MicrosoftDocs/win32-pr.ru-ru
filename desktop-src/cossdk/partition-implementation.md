---
description: При установке на сервере приложений COM+ автоматически создает секцию, называемую глобальным разделом.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Реализация секционирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130b1d2daeddee28b01271aa6b767ebc5a7eac5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710773"
---
# <a name="partition-implementation"></a><span data-ttu-id="63fcb-103">Реализация секционирования</span><span class="sxs-lookup"><span data-stu-id="63fcb-103">Partition Implementation</span></span>

<span data-ttu-id="63fcb-104">При установке на сервере приложений COM+ автоматически создает секцию, называемую *глобальным разделом*.</span><span class="sxs-lookup"><span data-stu-id="63fcb-104">When installed on an application server, COM+ automatically creates a partition, known as the *global partition*.</span></span> <span data-ttu-id="63fcb-105">Глобальный раздел включает стандартный набор приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="63fcb-105">The global partition includes a standard set of COM+ applications.</span></span> <span data-ttu-id="63fcb-106">Приложения COM+, установленные в глобальном разделе, автоматически становятся доступными для всех пользователей на сервере.</span><span class="sxs-lookup"><span data-stu-id="63fcb-106">COM+ applications that are installed in the global partition are automatically available to all users on the server.</span></span> <span data-ttu-id="63fcb-107">Если у вас есть другие приложения COM+, которые вы хотите сделать доступными для всех пользователей на сервере, их можно добавить в глобальный раздел.</span><span class="sxs-lookup"><span data-stu-id="63fcb-107">If you have other COM+ applications that you would like to make available to all users on the server, you can add them into the global partition.</span></span>

<span data-ttu-id="63fcb-108">В дополнение к глобальному разделу можно создавать другие разделы для пользователей только на этом сервере или для пользователей в домене.</span><span class="sxs-lookup"><span data-stu-id="63fcb-108">In addition to the global partition, you can create other partitions for users on that server only, or for users throughout the domain.</span></span> <span data-ttu-id="63fcb-109">Создание дополнительных разделов и установка в них нескольких конфигураций приложения COM+ позволяет пользователям одновременно выполнять эти конфигурации приложений на одном компьютере.</span><span class="sxs-lookup"><span data-stu-id="63fcb-109">Creating additional partitions and installing multiple configurations of a COM+ application into them allows your users to execute those application configurations simultaneously on the same computer.</span></span> <span data-ttu-id="63fcb-110">Кроме того, установка приложений COM+ в раздел, отличный от глобального раздела, позволяет управлять доступом пользователей к этим приложениям.</span><span class="sxs-lookup"><span data-stu-id="63fcb-110">Also, by installing COM+ applications into a partition other than the global partition, you can control user access to those applications.</span></span>

<span data-ttu-id="63fcb-111">**Windows XP:** Возможность создания, настройки или делегирования разделов COM+ недоступна.</span><span class="sxs-lookup"><span data-stu-id="63fcb-111">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="63fcb-112">Глобальный раздел является единственным доступным разделом COM+.</span><span class="sxs-lookup"><span data-stu-id="63fcb-112">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="63fcb-113">Дополнительные сведения о локальных секциях и секциях, определенных в Active Directory, см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="63fcb-113">For more information on local partitions and partitions defined within Active Directory, see the following topics:</span></span>

-   [<span data-ttu-id="63fcb-114">Локальные секции</span><span class="sxs-lookup"><span data-stu-id="63fcb-114">Local Partitions</span></span>](local-partitions.md)
-   [<span data-ttu-id="63fcb-115">Секции и Active Directory</span><span class="sxs-lookup"><span data-stu-id="63fcb-115">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
-   [<span data-ttu-id="63fcb-116">Секции по умолчанию</span><span class="sxs-lookup"><span data-stu-id="63fcb-116">Default Partitions</span></span>](default-partitions.md)
-   [<span data-ttu-id="63fcb-117">Глобальный раздел</span><span class="sxs-lookup"><span data-stu-id="63fcb-117">The Global Partition</span></span>](the-global-partition.md)
-   [<span data-ttu-id="63fcb-118">Свойства секции</span><span class="sxs-lookup"><span data-stu-id="63fcb-118">Partition Properties</span></span>](partition-properties.md)

## <a name="related-topics"></a><span data-ttu-id="63fcb-119">См. также</span><span class="sxs-lookup"><span data-stu-id="63fcb-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63fcb-120">Ограничения разработки приложений</span><span class="sxs-lookup"><span data-stu-id="63fcb-120">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="63fcb-121">Компоненты и разделы, помещенные в очередь COM+</span><span class="sxs-lookup"><span data-stu-id="63fcb-121">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="63fcb-122">Регистрация и Активация компонентов в секциях</span><span class="sxs-lookup"><span data-stu-id="63fcb-122">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="63fcb-123">Что такое разделы COM+?</span><span class="sxs-lookup"><span data-stu-id="63fcb-123">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



