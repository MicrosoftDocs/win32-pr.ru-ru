---
title: Элементы управления (COM)
description: Элементы управления
ms.assetid: 73947c81-6727-4112-9da0-efa60360f458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f440fff8f855f70c1a5ab3df78a6f6f6ed365ea
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104339995"
---
# <a name="controls-com"></a><span data-ttu-id="f8351-103">Элементы управления (COM)</span><span class="sxs-lookup"><span data-stu-id="f8351-103">Controls (COM)</span></span>

<span data-ttu-id="f8351-104">Элемент управления ActiveX — это просто еще один термин для объекта OLE или, точнее, COM-объект.</span><span class="sxs-lookup"><span data-stu-id="f8351-104">An ActiveX control is really just another term for OLE object or more specifically, COM object.</span></span> <span data-ttu-id="f8351-105">Другими словами, элемент управления, по крайней мере, является объектом COM, поддерживающим интерфейс [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) и который также является саморегистрируемым.</span><span class="sxs-lookup"><span data-stu-id="f8351-105">In other words, a control, at the very least, is some COM object that supports the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface and is also self-registering.</span></span> <span data-ttu-id="f8351-106">С помощью [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) контейнер может управлять временем существования элемента управления, а также динамически обнаруживать полную область функциональных возможностей элемента управления на основе доступных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="f8351-106">Through [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) a container can manage the lifetime of the control as well as dynamically discover the full extent of a control's functionality based on the available interfaces.</span></span> <span data-ttu-id="f8351-107">Это позволяет элементу управления реализовать как можно меньше функциональных возможностей, чем при необходимости, вместо поддержки большого количества интерфейсов, которые фактически не выполняют никаких действий.</span><span class="sxs-lookup"><span data-stu-id="f8351-107">This allows a control to implement as little functionality as it needs to, instead of supporting a large number of interfaces that actually don't do anything.</span></span> <span data-ttu-id="f8351-108">Короче говоря, это минимальное требование для всех элементов, не превышающих **IUnknown** , позволяет любому элементу управления быть как можно более простым.</span><span class="sxs-lookup"><span data-stu-id="f8351-108">In short, this minimal requirement for nothing more than **IUnknown** allows any control to be as lightweight as it can.</span></span>

<span data-ttu-id="f8351-109">Вкратце, за исключением [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) и самостоятельной регистрации, нет других требований к элементу управления.</span><span class="sxs-lookup"><span data-stu-id="f8351-109">In short, other than [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and self-registration, there are no other requirements for a control.</span></span> <span data-ttu-id="f8351-110">Однако существуют соглашения, которые следует соблюдать, чтобы обеспечить поддержку интерфейса с точки зрения функциональных возможностей, предоставляемых контейнером элементом управления.</span><span class="sxs-lookup"><span data-stu-id="f8351-110">There are, however, conventions that should be followed about what the support of an interface means in terms of functionality provided to the container by the control.</span></span> <span data-ttu-id="f8351-111">В этом разделе описывается, что означает элемент управления для фактической поддержки интерфейса, а также методы, свойства и события, которые элемент управления должен предоставить в качестве базового, если он может поддерживать методы, свойства и события.</span><span class="sxs-lookup"><span data-stu-id="f8351-111">This section then describes what it means for a control to actually support an interface, as well as methods, properties, and events that a control should provide as a baseline if it has occasion to support methods, properties, and events.</span></span>

<span data-ttu-id="f8351-112">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="f8351-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="f8351-113">Самостоятельная регистрация для элементов управления</span><span class="sxs-lookup"><span data-stu-id="f8351-113">Self Registration for Controls</span></span>](self-registration-for-controls.md)
-   [<span data-ttu-id="f8351-114">Поддержка интерфейса означает</span><span class="sxs-lookup"><span data-stu-id="f8351-114">What Support for an Interface Means</span></span>](what-support-for-an-interface-means.md)
-   [<span data-ttu-id="f8351-115">Интерфейсы сохраняемости</span><span class="sxs-lookup"><span data-stu-id="f8351-115">Persistence Interfaces</span></span>](persistence-interfaces.md)
-   [<span data-ttu-id="f8351-116">Необязательные методы в интерфейсах управления</span><span class="sxs-lookup"><span data-stu-id="f8351-116">Optional Methods in Control Interfaces</span></span>](optional-methods-in-control-interfaces.md)
-   [<span data-ttu-id="f8351-117">Параметры фабрики класса</span><span class="sxs-lookup"><span data-stu-id="f8351-117">Class Factory Options</span></span>](class-factory-options.md)
-   [<span data-ttu-id="f8351-118">Предоставление свойств через IDispatch</span><span class="sxs-lookup"><span data-stu-id="f8351-118">Exposing Properties through IDispatch</span></span>](properties.md)
-   [<span data-ttu-id="f8351-119">Предоставление доступа к методам через IDispatch</span><span class="sxs-lookup"><span data-stu-id="f8351-119">Exposing Methods through IDispatch</span></span>](exposing-methods-through-idispatch.md)
-   [<span data-ttu-id="f8351-120">События в элементах управления</span><span class="sxs-lookup"><span data-stu-id="f8351-120">Events in Controls</span></span>](events-in-controls.md)
-   [<span data-ttu-id="f8351-121">Страницы свойств</span><span class="sxs-lookup"><span data-stu-id="f8351-121">Property Pages</span></span>](property-pages.md)
-   [<span data-ttu-id="f8351-122">Свойства окружения для элементов управления</span><span class="sxs-lookup"><span data-stu-id="f8351-122">Ambient Properties for Controls</span></span>](ambient-properties-for-controls.md)
-   [<span data-ttu-id="f8351-123">Использование функциональных возможностей контейнера</span><span class="sxs-lookup"><span data-stu-id="f8351-123">Using the Container's Functionality</span></span>](using-the-container-s-functionality.md)

## <a name="related-topics"></a><span data-ttu-id="f8351-124">См. также</span><span class="sxs-lookup"><span data-stu-id="f8351-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8351-125">Рекомендации по контейнерам элементов управления и элементов управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="f8351-125">ActiveX Control and Control Container Guidelines</span></span>](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




