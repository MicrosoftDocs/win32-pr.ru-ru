---
title: Инфраструктура Виневентс
description: Операционная система Microsoft Windows включает функцию под названием Виневентс, которая позволяет процессам и приложениям, работающим на рабочем столе Windows, обмениваться определенными сведениями.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8846582a6d18f304cc08e3cb13ddb444cb278d7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "103785556"
---
# <a name="winevents"></a><span data-ttu-id="85056-103">WinEvents</span><span class="sxs-lookup"><span data-stu-id="85056-103">WinEvents</span></span>

<span data-ttu-id="85056-104">Операционная система Microsoft Windows включает функцию под названием *виневентс*, которая позволяет процессам и приложениям, работающим на рабочем столе Windows, обмениваться определенными сведениями.</span><span class="sxs-lookup"><span data-stu-id="85056-104">The Microsoft Windows operating system includes a feature, called *WinEvents*, that enables processes and applications running on the Windows desktop to exchange certain types of information.</span></span> <span data-ttu-id="85056-105">Специальные средства, использующие Microsoft UI Automation и Microsoft Active Accessibility, являются основными пользователями Виневентс.</span><span class="sxs-lookup"><span data-stu-id="85056-105">Accessibility tools that use Microsoft UI Automation and Microsoft Active Accessibility are among the primary users of the WinEvents.</span></span>

<span data-ttu-id="85056-106">В контексте доступности поставщики автоматизации пользовательского интерфейса и серверы Microsoft Active Accessibility используют Виневентс для уведомления клиентов об изменениях в пользовательском интерфейсе приложения, например при создании или удалении элемента пользовательского интерфейса или изменении имени, состояния или значения элемента.</span><span class="sxs-lookup"><span data-stu-id="85056-106">In the context of accessibility, UI Automation providers and Microsoft Active Accessibility servers use WinEvents to notify clients of changes in an application UI, such as when a UI element has been created or destroyed, or when an element name, state, or value has changed.</span></span>

<span data-ttu-id="85056-107">В этом разделе приводятся рекомендации, рекомендации и примеры, помогающие клиентам справляться с Виневентс и помочь серверам определить, когда следует активировать соответствующий WinEvent.</span><span class="sxs-lookup"><span data-stu-id="85056-107">This section provides suggestions, guidelines, and examples to help clients handle WinEvents and to help servers determine when to trigger the appropriate WinEvent.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="85056-108">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="85056-108">In this section</span></span>

-   [<span data-ttu-id="85056-109">Что такое Виневентс?</span><span class="sxs-lookup"><span data-stu-id="85056-109">What Are WinEvents?</span></span>](what-are-winevents.md)
-   [<span data-ttu-id="85056-110">Регистрация функции-обработчика</span><span class="sxs-lookup"><span data-stu-id="85056-110">Registering a Hook Function</span></span>](registering-a-hook-function.md)
-   [<span data-ttu-id="85056-111">События системного уровня и Object-Level</span><span class="sxs-lookup"><span data-stu-id="85056-111">System-Level and Object-Level Events</span></span>](system-level-and-object-level-events.md)
-   [<span data-ttu-id="85056-112">Функции-обработчики в контексте и вне контекста</span><span class="sxs-lookup"><span data-stu-id="85056-112">In-Context and Out-of-Context Hook Functions</span></span>](in-context-and-out-of-context-hook-functions.md)
-   [<span data-ttu-id="85056-113">Защита от повторного входа в функции-ловушки</span><span class="sxs-lookup"><span data-stu-id="85056-113">Guarding Against Reentrancy in Hook Functions</span></span>](guarding-against-reentrancy-in-hook-functions.md)
-   [<span data-ttu-id="85056-114">Выделение идентификаторов WinEvent</span><span class="sxs-lookup"><span data-stu-id="85056-114">Allocation of WinEvent IDs</span></span>](allocation-of-winevent-ids.md)

<span data-ttu-id="85056-115">Общие сведения о процессе уведомления о событиях в Microsoft Active Accessibility см. в разделе [виневентс](winevents-overview.md) в [техническом обзоре](technical-overview.md).</span><span class="sxs-lookup"><span data-stu-id="85056-115">For an overview of the event notification process in Microsoft Active Accessibility, see [WinEvents](winevents-overview.md) in the [Technical Overview](technical-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="85056-116">См. также</span><span class="sxs-lookup"><span data-stu-id="85056-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85056-117">Общая инфраструктура</span><span class="sxs-lookup"><span data-stu-id="85056-117">Common Infrastructure</span></span>](common-infrastructure.md)
</dt> </dl>

 

 




