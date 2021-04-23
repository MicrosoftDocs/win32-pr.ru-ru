---
title: Элементы управления ActiveX
description: Элементы управления ActiveX
ms.assetid: e491b66c-d6ba-4476-8413-7a9e41c05e8d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b75aabfbf2b81b4a4d3a45a1868a6eebf6fd4e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413781"
---
# <a name="activex-controls"></a><span data-ttu-id="1279e-103">Элементы управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="1279e-103">ActiveX Controls</span></span>

<span data-ttu-id="1279e-104">Элементы управления ActiveX — это основы, состоящие из COM, доступных для подключения объектов, составных документов, страниц свойств, OLE-автоматизации, сохраняемости объектов и предоставляемых системой объектов шрифтов и изображений.</span><span class="sxs-lookup"><span data-stu-id="1279e-104">ActiveX controls technology rests on a foundation consisting of COM, connectable objects, compound documents, property pages, OLE automation, object persistence, and system-provided font and picture objects.</span></span> <span data-ttu-id="1279e-105">Как показано ниже, каждая из этих основных технологий играет роль в элементах управления.</span><span class="sxs-lookup"><span data-stu-id="1279e-105">As summarized below, each of these core technologies plays a role in controls.</span></span>

<dl> <dt>

<span data-ttu-id="1279e-106"><span id="COM"></span><span id="com"></span>-</span><span class="sxs-lookup"><span data-stu-id="1279e-106"><span id="COM"></span><span id="com"></span>COM</span></span>
</dt> <dd>

<span data-ttu-id="1279e-107">Элемент управления, по сути, является COM-объектом, предоставляющим интерфейс [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , через который клиенты могут получать указатели на другие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1279e-107">A control is essentially a COM object that exposes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, through which clients can obtain pointers to its other interfaces.</span></span> <span data-ttu-id="1279e-108">Элементы управления могут поддерживать лицензирование через [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) и самостоятельную регистрацию.</span><span class="sxs-lookup"><span data-stu-id="1279e-108">Controls can support licensing through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) and self-registration.</span></span> <span data-ttu-id="1279e-109">Дополнительные сведения об COM, лицензировании и самостоятельной регистрации см. [в разделе Объектная модель компонентов](the-component-object-model.md) .</span><span class="sxs-lookup"><span data-stu-id="1279e-109">See [The Component Object Model](the-component-object-model.md) for more information on COM, licensing, and self-registration.</span></span>

</dd> <dt>

<span data-ttu-id="1279e-110"><span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Подключаемые объекты</span><span class="sxs-lookup"><span data-stu-id="1279e-110"><span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Connectable objects</span></span>
</dt> <dd>

<span data-ttu-id="1279e-111">Элементы управления могут поддерживать исходящие интерфейсы через подключаемые объекты, чтобы элемент управления мог взаимодействовать со своим клиентом.</span><span class="sxs-lookup"><span data-stu-id="1279e-111">Controls can support outgoing interfaces through connectable objects so that the control can communicate with its client.</span></span> <span data-ttu-id="1279e-112">Например, исходящий интерфейс может активировать действие в клиенте, может уведомлять Клиента о некоторых изменениях в элементе управления или запрашивать разрешение у клиента до того, как элемент управления потребует какого бы то ни было действия.</span><span class="sxs-lookup"><span data-stu-id="1279e-112">For example, an outgoing interface can trigger an action in the client, can notify the client of some change in the control, or can request permission from the client before the control takes some action.</span></span> <span data-ttu-id="1279e-113">Дополнительные сведения о том, как работают подключаемые объекты, см. [в разделе события в com и Connected Objects](events-in-com-and-connectable-objects.md) .</span><span class="sxs-lookup"><span data-stu-id="1279e-113">See [Events in COM and Connectable Objects](events-in-com-and-connectable-objects.md) for more information on how connectable objects work.</span></span>

</dd> <dt>

<span data-ttu-id="1279e-114"><span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Единая для обмена данными</span><span class="sxs-lookup"><span data-stu-id="1279e-114"><span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform data transfer</span></span>
</dt> <dd>

<span data-ttu-id="1279e-115">Элементы управления могут быть перенесены и удалены в контейнере с помощью справки из их контейнера.</span><span class="sxs-lookup"><span data-stu-id="1279e-115">Controls can support being dragged and dropped within a container with help from their container.</span></span> <span data-ttu-id="1279e-116">Дополнительные сведения о перетаскивании см. в разделе [**иолеинплацеобжектвиндовлесс:: жетдроптаржет**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="1279e-116">See [**IOleInPlaceObjectWindowless::GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) for more information on drag and drop.</span></span>

</dd> <dt>

<span data-ttu-id="1279e-117"><span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Составные документы</span><span class="sxs-lookup"><span data-stu-id="1279e-117"><span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Compound documents</span></span>
</dt> <dd>

<span data-ttu-id="1279e-118">Элемент управления может быть встроенным активным объектом, который может быть внедрен в содержащий его клиент.</span><span class="sxs-lookup"><span data-stu-id="1279e-118">A control can be an in-place active object that can be embedded in a containing client.</span></span> <span data-ttu-id="1279e-119">Конечный пользователь активирует элемент управления для инициации действия в контейнерном приложении.</span><span class="sxs-lookup"><span data-stu-id="1279e-119">An end-user activates the control to initiate an action in the container application.</span></span> <span data-ttu-id="1279e-120">Дополнительные сведения об активации на месте и других интерфейсах составных документов см. в разделе [составные документы](compound-documents.md) .</span><span class="sxs-lookup"><span data-stu-id="1279e-120">See [Compound Documents](compound-documents.md) for more information on in-place activation and other compound document interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="1279e-121"><span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Страницы свойств</span><span class="sxs-lookup"><span data-stu-id="1279e-121"><span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Property pages</span></span>
</dt> <dd>

<span data-ttu-id="1279e-122">Элементы управления могут предоставлять страницы свойств, чтобы конечные пользователи могли просматривать и изменять свойства элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1279e-122">Controls can provide property pages so end users can view and change the control's properties.</span></span> <span data-ttu-id="1279e-123">Дополнительные сведения о работе страниц свойств см. в разделе [страницы свойств и вкладки свойств](property-pages-and-property-sheets.md) .</span><span class="sxs-lookup"><span data-stu-id="1279e-123">See [Property Pages and Property Sheets](property-pages-and-property-sheets.md) for more information on how property pages work.</span></span>

</dd> <dt>

<span data-ttu-id="1279e-124"><span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE Automation</span><span class="sxs-lookup"><span data-stu-id="1279e-124"><span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE automation</span></span>
</dt> <dd>

<span data-ttu-id="1279e-125">Элементы управления могут предоставлять возможности программирования с помощью OLE-автоматизации, чтобы клиенты могли воспользоваться преимуществами функций элемента управления через язык программирования, предоставляемый клиентом.</span><span class="sxs-lookup"><span data-stu-id="1279e-125">Controls can provide programmability through OLE automation so clients can take advantage of the control's features through a programming language supplied by the client.</span></span> <span data-ttu-id="1279e-126">Дополнительные сведения о OLE Automation см. в разделе OLE Automation.</span><span class="sxs-lookup"><span data-stu-id="1279e-126">See the OLE Automation section for more information on OLE automation.</span></span>

</dd> <dt>

<span data-ttu-id="1279e-127"><span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Постоянное хранилище</span><span class="sxs-lookup"><span data-stu-id="1279e-127"><span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Persistent storage</span></span>
</dt> <dd>

<span data-ttu-id="1279e-128">Элемент управления может реализовывать один или несколько интерфейсов сохраняемости для поддержки сохранения состояния.</span><span class="sxs-lookup"><span data-stu-id="1279e-128">A control can implement one or more of several persistence interfaces to support persistence of its state.</span></span> <span data-ttu-id="1279e-129">Разработчик элемента управления должен решить, какие типы сохраняемости наиболее важны, и реализовать соответствующие интерфейсы сохраняемости.</span><span class="sxs-lookup"><span data-stu-id="1279e-129">The control implementer must decide what kinds of persistence are most important and implement the appropriate persistence interfaces.</span></span> <span data-ttu-id="1279e-130">Клиент решает, какой интерфейс предпочтительнее использовать.</span><span class="sxs-lookup"><span data-stu-id="1279e-130">The client decides which interface it prefers to use.</span></span> <span data-ttu-id="1279e-131">Дополнительные сведения о всех интерфейсах сохраняемости см. [в разделе Объектная модель компонентов](the-component-object-model.md) .</span><span class="sxs-lookup"><span data-stu-id="1279e-131">See [The Component Object Model](the-component-object-model.md) for more information on all the persistence interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="1279e-132"><span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Объекты Font и Picture</span><span class="sxs-lookup"><span data-stu-id="1279e-132"><span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Font and picture objects</span></span>
</dt> <dd>

<span data-ttu-id="1279e-133">Элементы управления могут использовать эти предоставляемые системой объекты для предоставления визуального представления в пределах клиента.</span><span class="sxs-lookup"><span data-stu-id="1279e-133">Controls can use these system provided objects to provide a visual representation of themselves within the client.</span></span> <span data-ttu-id="1279e-134">Объект Font реализует несколько интерфейсов, включая [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) и [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp).</span><span class="sxs-lookup"><span data-stu-id="1279e-134">The font object implements several interfaces, including [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) and [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp).</span></span> <span data-ttu-id="1279e-135">Объект Font можно создать с помощью [**олекреатефонтиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect).</span><span class="sxs-lookup"><span data-stu-id="1279e-135">A font object can be created with [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect).</span></span> <span data-ttu-id="1279e-136">Объект Picture также реализует несколько интерфейсов, включая [**ипиктуре**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) и [**ипиктуредисп**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp).</span><span class="sxs-lookup"><span data-stu-id="1279e-136">The picture object also implements several interfaces, including [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) and [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp).</span></span> <span data-ttu-id="1279e-137">Объект Picture можно создать с помощью [**олекреатепиктуреиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) и загрузить из потока с помощью [**олелоадпиктуре**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).</span><span class="sxs-lookup"><span data-stu-id="1279e-137">A picture object can be created using [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) and can loaded from a stream with [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).</span></span>

</dd> </dl>

<span data-ttu-id="1279e-138">Важно понимать, что эти функции можно использовать в любом объекте OLE.</span><span class="sxs-lookup"><span data-stu-id="1279e-138">It is important to understand that these features can be used in any OLE object.</span></span> <span data-ttu-id="1279e-139">Для использования этих функций не требуется реализовывать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="1279e-139">One does not need to implement a control in order to use these features.</span></span> <span data-ttu-id="1279e-140">Кроме того, единственным необходимым интерфейсом для элемента управления является IUnknown.</span><span class="sxs-lookup"><span data-stu-id="1279e-140">Also, the only required interface on a control is IUnknown.</span></span> <span data-ttu-id="1279e-141">Элемент управления дополнительно поддерживает другие интерфейсы в зависимости от необходимости поддержки связанных функций.</span><span class="sxs-lookup"><span data-stu-id="1279e-141">The control optionally supports other interfaces based on the need to support the related features.</span></span>

<span data-ttu-id="1279e-142">Помимо этих функций, следующие интерфейсы и функции относятся к технологиям элементов управления: [**метод интерфейса IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**исимплефрамесите**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)и [**олетранслатеколор**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor).</span><span class="sxs-lookup"><span data-stu-id="1279e-142">In addition to these features, the following interfaces and functions are specific to controls technology: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), and [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor).</span></span> <span data-ttu-id="1279e-143">Кроме того, конкретные элементы управления представляют собой набор стандартов для свойств и методов, которые могут поддерживаться элементом управления или контейнером элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1279e-143">Also specific to controls are a set of standards for properties and methods that a control or a control container can support.</span></span>

> [!Note]  
> <span data-ttu-id="1279e-144">Системная библиотека OleAut32.dll содержит реализации функций ([**олекреатепропертифраме**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**олекреатепропертифрамеиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**олекреатефонтиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**олекреатепиктуреиндирект**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)и [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)).</span><span class="sxs-lookup"><span data-stu-id="1279e-144">The system library OleAut32.dll contains implementations of the functions ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture), and [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)).</span></span> <span data-ttu-id="1279e-145">Кроме того, OleAut32.dll содержит реализации стандартных объектов Font и Picture, а также библиотеку типов для всех интерфейсов, используемых с элементами управления, а также дополнительные структуры данных и типы данных.</span><span class="sxs-lookup"><span data-stu-id="1279e-145">In addition, OleAut32.dll contains the implementations of the standard font and picture objects, as well as a type library for all the interfaces used with controls as well as the additional data structures and data types.</span></span>

 

<span data-ttu-id="1279e-146">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="1279e-146">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="1279e-147">Архитектура элементов управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="1279e-147">ActiveX Controls Architecture</span></span>](activex-controls-architecture.md)
-   [<span data-ttu-id="1279e-148">Интерфейсы элементов управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="1279e-148">ActiveX Controls Interfaces</span></span>](activex-controls-interfaces.md)
-   [<span data-ttu-id="1279e-149">Свойства и методы</span><span class="sxs-lookup"><span data-stu-id="1279e-149">Properties and Methods</span></span>](properties-and-methods.md)
-   [<span data-ttu-id="1279e-150">События элементов управления</span><span class="sxs-lookup"><span data-stu-id="1279e-150">Control Events</span></span>](control-events.md)
-   [<span data-ttu-id="1279e-151">Визуальное представление</span><span class="sxs-lookup"><span data-stu-id="1279e-151">Visual Representation</span></span>](visual-representation.md)
-   [<span data-ttu-id="1279e-152">Обработка клавиатуры для элементов управления</span><span class="sxs-lookup"><span data-stu-id="1279e-152">Keyboard Handling for Controls</span></span>](keyboard-handling-for-controls.md)
-   [<span data-ttu-id="1279e-153">Сохраняемость</span><span class="sxs-lookup"><span data-stu-id="1279e-153">Persistence</span></span>](persistence.md)
-   [<span data-ttu-id="1279e-154">Регистрация и лицензирование</span><span class="sxs-lookup"><span data-stu-id="1279e-154">Registration and Licensing</span></span>](registration-and-licensing.md)

## <a name="related-topics"></a><span data-ttu-id="1279e-155">См. также</span><span class="sxs-lookup"><span data-stu-id="1279e-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1279e-156">Рекомендации по контейнерам элементов управления и элементов управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="1279e-156">ActiveX Control and Control Container Guidelines</span></span>](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 