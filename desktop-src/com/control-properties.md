---
title: Свойства элемента управления
description: Свойства элемента управления
ms.assetid: 29c2cca3-9460-45d1-9591-026e8c18f26f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4749a7a7e408f6cd58951a72207ed801e4104d65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889136"
---
# <a name="control-properties"></a><span data-ttu-id="68adf-103">Свойства элемента управления</span><span class="sxs-lookup"><span data-stu-id="68adf-103">Control Properties</span></span>

<span data-ttu-id="68adf-104">Помимо свойств, определенных и реализованных самим элементом управления, технология элементов управления ActiveX также включает:</span><span class="sxs-lookup"><span data-stu-id="68adf-104">In addition to properties defined and implemented by the control itself, ActiveX controls technology also involves:</span></span>

<dl> <dt>

<span data-ttu-id="68adf-105"><span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Свойства окружения</span><span class="sxs-lookup"><span data-stu-id="68adf-105"><span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Ambient properties</span></span>
</dt> <dd>

<span data-ttu-id="68adf-106">Они предоставляются контейнером через клиентский сайт элемента управления для предоставления значений окружающей среды, которые применяются ко всем элементам управления, внедренным в контейнер.</span><span class="sxs-lookup"><span data-stu-id="68adf-106">These are exposed by the container through a control client site to provide environmental values that apply to all controls embedded in the container.</span></span> <span data-ttu-id="68adf-107">Например, контейнер может предоставить цвет фона по умолчанию или шрифт по умолчанию, который может использоваться элементом управления.</span><span class="sxs-lookup"><span data-stu-id="68adf-107">For example, a container can provide a default background color or a default font that the control can use.</span></span> <span data-ttu-id="68adf-108">Свойства окружения предоставляются через интерфейс **IDispatch** , реализованный в объекте-сайте контейнера.</span><span class="sxs-lookup"><span data-stu-id="68adf-108">Ambient properties are exposed through **IDispatch** implemented on a container's site object.</span></span> <span data-ttu-id="68adf-109">Контейнер вызывает метод [**метод интерфейса IOleControl:: онамбиентпропертичанже**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) элемента управления, когда любое из его свойств окружения изменяет значение.</span><span class="sxs-lookup"><span data-stu-id="68adf-109">The container calls the control's [**IOleControl::OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) method when any of its ambient properties change value.</span></span> <span data-ttu-id="68adf-110">В ответе элементу управления может потребоваться обновить собственное внутреннее или визуальное состояние в ответе.</span><span class="sxs-lookup"><span data-stu-id="68adf-110">In response, a control may need to update its own internal or visual state in response.</span></span> <span data-ttu-id="68adf-111">Контейнер указывает, какое внешнее свойство изменилось с помощью параметра DISPID, или передать DISPID \_ Unknown, чтобы указать, что изменилось несколько внешних свойств.</span><span class="sxs-lookup"><span data-stu-id="68adf-111">The container indicates which ambient property changed with the DISPID parameter or may pass DISPID\_UNKNOWN to indicate that multiple ambient properties changed.</span></span>

</dd> <dt>

<span data-ttu-id="68adf-112"><span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Расширенные свойства</span><span class="sxs-lookup"><span data-stu-id="68adf-112"><span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Extended properties</span></span>
</dt> <dd>

<span data-ttu-id="68adf-113">Фактически они реализуются контейнером для заключения элементов управления, которые он содержит, для предоставления свойств, управляемых контейнером, которые отображаются как свойства собственного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="68adf-113">These are actually implemented by a container to wrap the controls it contains to provide container-managed properties that appear as if they were native control properties.</span></span> <span data-ttu-id="68adf-114">Контейнер может выполнять статистическую обработку элемента управления, добавляя расширенные свойства в дополнение или переопределяя свойства элемента управления.</span><span class="sxs-lookup"><span data-stu-id="68adf-114">The container can aggregate the control, adding the extended properties to supplement or override the control's properties.</span></span> <span data-ttu-id="68adf-115">Агрегированный объект называется расширенным элементом управления.</span><span class="sxs-lookup"><span data-stu-id="68adf-115">The aggregated object is called an extended control.</span></span> <span data-ttu-id="68adf-116">В контейнере расширенный элемент управления отображается как сам элемент управления, а расширенные свойства должны предоставляться элементом управления.</span><span class="sxs-lookup"><span data-stu-id="68adf-116">To the container, the extended control appears as the control itself and extended properties appear to be exposed by the control.</span></span> <span data-ttu-id="68adf-117">Контейнер поддерживает расширенный контроль с помощью метода клиентского сайта [**IOleControlSite:: жетекстендедконтрол**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol).</span><span class="sxs-lookup"><span data-stu-id="68adf-117">The container supports an extended control through its client site method [**IOleControlSite::GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol).</span></span> <span data-ttu-id="68adf-118">Метод **жетекстендедконтрол** позволяет элементам управления перемещаться по сайту к объекту расширенного элемента управления, предоставляемому контейнером, если контейнер поддерживает эту функцию.</span><span class="sxs-lookup"><span data-stu-id="68adf-118">The **GetExtendedControl** method allows controls to navigate through the site to the extended control object provided for them by the container, if the container supports this feature.</span></span> <span data-ttu-id="68adf-119">Контейнер может также отображать страницы свойств для расширенных элементов управления в дополнение к страницам, которые элемент управления обычно задает с помощью [**испеЦифипропертипажес**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages).</span><span class="sxs-lookup"><span data-stu-id="68adf-119">A container can also choose to show property pages for its extended controls in addition to those pages that a control would normally specify through [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages).</span></span> <span data-ttu-id="68adf-120">По этой причине элемент управления должен задать контейнер для отображения рамки свойства, прежде чем элемент управления попытается сделать это.</span><span class="sxs-lookup"><span data-stu-id="68adf-120">Because of this, a control has to ask a container to show a property frame before the control attempts to do so itself.</span></span> <span data-ttu-id="68adf-121">Для этого элемент управления вызывает [**IOleControlSite:: шовпропертифраме**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) .</span><span class="sxs-lookup"><span data-stu-id="68adf-121">The control calls [**IOleControlSite::ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) to do this.</span></span> <span data-ttu-id="68adf-122">Если контейнер реализует эту функцию, он отображает саму рамку свойства; Если метод возвращает ошибку, то элемент управления может отобразить рамку свойства.</span><span class="sxs-lookup"><span data-stu-id="68adf-122">If the container implements this function then it shows the property frame itself; if the method returns an error then the control can show the property frame.</span></span>

</dd> </dl>

<span data-ttu-id="68adf-123">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="68adf-123">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="68adf-124">Стандартные свойства</span><span class="sxs-lookup"><span data-stu-id="68adf-124">Standard Properties</span></span>](standard-properties.md)
-   [<span data-ttu-id="68adf-125">Объект стандартного шрифта</span><span class="sxs-lookup"><span data-stu-id="68adf-125">Standard Font Object</span></span>](standard-font-object.md)
-   [<span data-ttu-id="68adf-126">Стандартный объект Picture</span><span class="sxs-lookup"><span data-stu-id="68adf-126">Standard Picture Object</span></span>](standard-picture-object.md)

## <a name="related-topics"></a><span data-ttu-id="68adf-127">См. также</span><span class="sxs-lookup"><span data-stu-id="68adf-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68adf-128">Методы управления</span><span class="sxs-lookup"><span data-stu-id="68adf-128">Control Methods</span></span>](control-methods.md)
</dt> </dl>

 

 




