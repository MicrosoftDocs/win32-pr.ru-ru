---
title: Архитектура элементов управления ActiveX
description: Технологии элементов управления ActiveX основаны на различных объектах и интерфейсах более низкого уровня в OLE. Конкретные интерфейсы, доступные в элементе управления, зависят от его возможностей. Этот раздел подробно рассматривает возможности, предоставляемые элементом управления.
ms.assetid: 42959a11-8bfb-4f7e-ba27-5dc1ed49cdaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0592d774e1930623803d0769fb7890709a2f21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775089"
---
# <a name="activex-controls-architecture"></a><span data-ttu-id="f5f8b-105">Архитектура элементов управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="f5f8b-105">ActiveX Controls Architecture</span></span>

<span data-ttu-id="f5f8b-106">Технологии элементов управления ActiveX основаны на различных объектах и интерфейсах более низкого уровня в OLE.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-106">ActiveX controls technology builds on a foundation of many lower-level objects and interfaces in OLE.</span></span> <span data-ttu-id="f5f8b-107">Конкретные интерфейсы, доступные в элементе управления, зависят от его возможностей.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-107">The exact interfaces available on a control vary with its capabilities.</span></span> <span data-ttu-id="f5f8b-108">Этот раздел подробно рассматривает возможности, предоставляемые элементом управления.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-108">This section takes a closer look at the capabilities a control might provide.</span></span>

<span data-ttu-id="f5f8b-109">Элементы управления ActiveX используются для предоставления стандартных блоков для создания пользовательских интерфейсов в приложениях.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-109">ActiveX controls are used to provide the building blocks for creating user interfaces in applications.</span></span> <span data-ttu-id="f5f8b-110">Например, кнопка, инициирующая некоторое действие в приложении-контейнере при его щелчке, является простым элементом управления.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-110">For example, a button that initiates some action in the container application when it is clicked is a simple control.</span></span> <span data-ttu-id="f5f8b-111">При предоставлении этих стандартных блоков пользовательского интерфейса участвуют следующие аспекты.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-111">The following aspects are involved in providing these user interface building blocks:</span></span>

-   <span data-ttu-id="f5f8b-112">Элемент управления может быть внедрен в клиент контейнера для поддержки некоторой активности пользовательского интерфейса в клиенте.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-112">A control can be embedded within its container client to support some user interface activity within the client.</span></span> <span data-ttu-id="f5f8b-113">Таким образом, элементу управления необходимо предоставить визуальное представление самого себя, если оно встроено в контейнер, и необходимо предоставить способ сохранения его состояния, например его значения свойств и его расположение в контейнере.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-113">Thus, a control needs to provide a visual representation of itself when it is embedded within the container and needs to provide a way to save its state, for example, its property values and its position within its container.</span></span> <span data-ttu-id="f5f8b-114">Клиент должен поддерживать контейнер с внедренными в него объектами.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-114">The client must support being a container with objects embedded in it.</span></span>
-   <span data-ttu-id="f5f8b-115">При активации элемента управления с помощью клавиатуры или мыши конечный пользователь инициирует какое-либо действие в клиентском приложении.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-115">By activating the control using a keyboard or mouse, the end user initiates some action in the client application.</span></span> <span data-ttu-id="f5f8b-116">Таким образом, элемент управления должен реагировать на действие клавиатуры и должен иметь возможность взаимодействовать с его клиентом, чтобы он мог уведомлять его контейнер действий и запускать события в клиенте.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-116">Thus, a control must respond to keyboard activity and must be able to communicate with its client so it can notify its container of its activities and trigger events in the client.</span></span>
-   <span data-ttu-id="f5f8b-117">Клиент также обычно предоставляет язык программирования, с помощью которого конечный пользователь может инициировать действия, предоставляемые свойствами и методами элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-117">The client also typically provides a programming language through which the end user can initiate actions provided by the control's properties and methods.</span></span> <span data-ttu-id="f5f8b-118">Таким образом, элемент управления должен поддерживать автоматизацию и некоторый набор функций времени разработки и времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-118">Thus, a control must support automation and some set of design-time versus run-time features as well.</span></span>

<span data-ttu-id="f5f8b-119">В результате его роли в создании стандартных блоков пользовательского интерфейса элемент управления обычно поддерживает функции в следующих областях, используя технологии OLE, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="f5f8b-119">As a result of its role in providing user interface building blocks, a control typically supports features in the following areas using OLE technologies as indicated:</span></span>

<dl> <dt>

<span data-ttu-id="f5f8b-120"><span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Свойства и методы</span><span class="sxs-lookup"><span data-stu-id="f5f8b-120"><span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Properties and methods</span></span>
</dt> <dd>

<span data-ttu-id="f5f8b-121">Как и любой объект OLE, элемент управления может обеспечить большую часть его функциональных возможностей с помощью набора входящих интерфейсов со свойствами и методами.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-121">Like any OLE object, a control can provide much of its functionality through a set of incoming interfaces with properties and methods.</span></span> <span data-ttu-id="f5f8b-122">Контейнер может предоставлять дополнительные свойства окружения, а также поддерживает расширение свойств элемента управления с помощью статистической обработки.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-122">The container can supply additional ambient properties, and it can support extending the control's properties through aggregation.</span></span> <span data-ttu-id="f5f8b-123">Эти функции разкрываются на OLE Automation, страницах свойств, подключаемых объектах и технологиях элементов управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-123">These features rest on OLE automation, property pages, connectable objects, and ActiveX control technologies.</span></span>

</dd> <dt>

<span data-ttu-id="f5f8b-124"><span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Событиях</span><span class="sxs-lookup"><span data-stu-id="f5f8b-124"><span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Events</span></span>
</dt> <dd>

<span data-ttu-id="f5f8b-125">Помимо предоставления свойств и методов, элемент управления ActiveX также может предоставлять исходящие интерфейсы для уведомления клиента о событиях.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-125">In addition to providing properties and methods, an ActiveX control can also provide outgoing interfaces to notify its client of events.</span></span> <span data-ttu-id="f5f8b-126">Клиент должен поддерживать обработку этих событий.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-126">The client must support handling of these events.</span></span> <span data-ttu-id="f5f8b-127">Эти функции используют OLE Automation и подключаемые объекты.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-127">These features use OLE automation and connectable objects.</span></span>

</dd> <dt>

<span data-ttu-id="f5f8b-128"><span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Визуальное представление</span><span class="sxs-lookup"><span data-stu-id="f5f8b-128"><span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Visual representation</span></span>
</dt> <dd>

<span data-ttu-id="f5f8b-129">Элемент управления может поддерживать размещение и отображение самого себя в своем контейнере.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-129">A control can support positioning and displaying itself within its container.</span></span> <span data-ttu-id="f5f8b-130">Контейнер помещает элемент управления и определяет его размер.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-130">The container positions the control and determines its size.</span></span> <span data-ttu-id="f5f8b-131">Эти функции используют технологию составного документа, в том числе технологию перетаскивания OLE.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-131">These features use compound document technology, including OLE drag and drop technology.</span></span>

</dd> <dt>

<span data-ttu-id="f5f8b-132"><span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Обработка с помощью клавиатуры</span><span class="sxs-lookup"><span data-stu-id="f5f8b-132"><span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Keyboard handling</span></span>
</dt> <dd>

<span data-ttu-id="f5f8b-133">Элемент управления может реагировать на сочетания клавиш, чтобы конечный пользователь мог инициировать действия, выполняемые элементом управления.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-133">A control can respond to keyboard accelerators so the end-user can initiate actions performed by the control.</span></span> <span data-ttu-id="f5f8b-134">Контейнер управляет работой клавиатуры для всех его внедренных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-134">The container manages keyboard activity for all its embedded controls.</span></span> <span data-ttu-id="f5f8b-135">Эти функции используют технологии управления и объединения документов.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-135">These features use control and compound document technologies.</span></span>

</dd> <dt>

<span data-ttu-id="f5f8b-136"><span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Сохраняемости</span><span class="sxs-lookup"><span data-stu-id="f5f8b-136"><span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistence</span></span>
</dt> <dd>

<span data-ttu-id="f5f8b-137">Элемент управления может сохранить свое состояние.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-137">A control can save its state.</span></span> <span data-ttu-id="f5f8b-138">Клиент управляет сохраняемостью своих внедренных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-138">The client manages the persistence of its embedded controls.</span></span> <span data-ttu-id="f5f8b-139">Эти функции используют структурированные технологии хранения и сохранения объектов.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-139">These features use structured storage and object persistence technologies.</span></span>

</dd> <dt>

<span data-ttu-id="f5f8b-140"><span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Регистрация и лицензирование</span><span class="sxs-lookup"><span data-stu-id="f5f8b-140"><span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registration and licensing</span></span>
</dt> <dd>

<span data-ttu-id="f5f8b-141">Элемент управления обычно поддерживает самостоятельную регистрацию и создает набор записей реестра при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-141">A control typically supports self-registration and creates a set of registry entries when it is instantiated.</span></span> <span data-ttu-id="f5f8b-142">Элемент управления также может быть лицензирован для предотвращения несанкционированного использования.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-142">A control can also be licensed to help prevent unauthorized use.</span></span>

</dd> </dl>

<span data-ttu-id="f5f8b-143">Большинство этих функций используют как элемент управления, так и его контейнер клиента.</span><span class="sxs-lookup"><span data-stu-id="f5f8b-143">Most of these features involve both the control and its client container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5f8b-144">См. также</span><span class="sxs-lookup"><span data-stu-id="f5f8b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5f8b-145">Элементы управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="f5f8b-145">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




