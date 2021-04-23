---
title: Сообщение WM_GETOBJECT (Winuser. h)
description: Посылается как Microsoft Active Accessibility, так и Microsoft UI Automation для получения сведений о доступном объекте, который содержится в серверном приложении.
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- Специальные WM_GETOBJECT сообщения Windows
topic_type:
- apiref
api_name:
- WM_GETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcac5c7f6dd8203c32b9f6f3c4eb59144cc3f8ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137755"
---
# <a name="wm_getobject-message"></a><span data-ttu-id="46d2e-104">\_Сообщение WM GetObject</span><span class="sxs-lookup"><span data-stu-id="46d2e-104">WM\_GETOBJECT message</span></span>

<span data-ttu-id="46d2e-105">Посылается как Microsoft Active Accessibility, так и Microsoft UI Automation для получения сведений о доступном объекте, который содержится в серверном приложении.</span><span class="sxs-lookup"><span data-stu-id="46d2e-105">Sent by both Microsoft Active Accessibility and Microsoft UI Automation to obtain information about an accessible object contained in a server application.</span></span>

<span data-ttu-id="46d2e-106">Приложения никогда не отправляют это сообщение напрямую.</span><span class="sxs-lookup"><span data-stu-id="46d2e-106">Applications never send this message directly.</span></span> <span data-ttu-id="46d2e-107">Microsoft Active Accessibility отправляет это сообщение в ответ на вызовы [**акцессиблеобжектфромпоинт**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**акцессиблеобжектфромевент**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)или [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="46d2e-107">Microsoft Active Accessibility sends this message in response to calls to [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), or [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span> <span data-ttu-id="46d2e-108">Однако серверные приложения обработают это сообщение.</span><span class="sxs-lookup"><span data-stu-id="46d2e-108">However, server applications handle this message.</span></span> <span data-ttu-id="46d2e-109">Модель автоматизации пользовательского интерфейса отправляет это сообщение в ответ на вызовы [**иуиаутоматион:: елементфромхандле**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**елементфромпоинт**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)и [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), а при обработке событий, для которых зарегистрирован клиент.</span><span class="sxs-lookup"><span data-stu-id="46d2e-109">UI Automation sends this message in response to calls to [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint), and [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), and when handling events for which a client has registered.</span></span>


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a><span data-ttu-id="46d2e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="46d2e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46d2e-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="46d2e-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="46d2e-112">Предоставляет дополнительные сведения о сообщении и используется только системой.</span><span class="sxs-lookup"><span data-stu-id="46d2e-112">Provides additional information about the message and is used only by the system.</span></span> <span data-ttu-id="46d2e-113">Серверы передают *dwFlags* в качестве параметра *wParam* в вызове [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) при обработке сообщения.</span><span class="sxs-lookup"><span data-stu-id="46d2e-113">Servers pass *dwFlags* as the *wParam* parameter in the call to [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) when handling the message.</span></span>

</dd> <dt>

<span data-ttu-id="46d2e-114">*двобжид*</span><span class="sxs-lookup"><span data-stu-id="46d2e-114">*dwObjId*</span></span> 
</dt> <dd>

<span data-ttu-id="46d2e-115">Идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="46d2e-115">Object identifier.</span></span> <span data-ttu-id="46d2e-116">Это значение является одной из констант [идентификатора объекта](object-identifiers.md) или идентификатором пользовательского объекта.</span><span class="sxs-lookup"><span data-stu-id="46d2e-116">This value is one of the [object identifier](object-identifiers.md) constants or a custom object identifier.</span></span> <span data-ttu-id="46d2e-117">Серверное приложение должно проверить это значение, чтобы определить тип запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="46d2e-117">A server application must check this value to identify the type of information being requested.</span></span> <span data-ttu-id="46d2e-118">Прежде чем сравнивать это значение со \_ ЗНАЧЕНИЯМИ OBJID, сервер должен привести его к типу **DWORD**. в противном случае в 64-разрядной системе Windows расширение знака *lParam* может помешать сравнению.</span><span class="sxs-lookup"><span data-stu-id="46d2e-118">Before comparing this value against the OBJID\_ values, the server must cast it to **DWORD**; otherwise, on 64-bit Windows, the sign extension of the *lParam* can interfere with the comparison.</span></span>

-   <span data-ttu-id="46d2e-119">Если *двобжид* является одним из значений OBJID \_ , таких как [**OBJID \_ Client**](object-identifiers.md), то запрос предназначен для объекта Microsoft Active Accessibility, который реализует [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="46d2e-119">If *dwObjId* is one of the OBJID\_ values such as [**OBJID\_CLIENT**](object-identifiers.md), the request is for a Microsoft Active Accessibility object that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span>
-   <span data-ttu-id="46d2e-120">Если *двобжид* равен **уиарутобжектид**, то запрос предназначен для поставщика автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="46d2e-120">If *dwObjId* is equal to **UiaRootObjectId**, the request is for a UI Automation provider.</span></span> <span data-ttu-id="46d2e-121">Если сервер реализует автоматизацию пользовательского интерфейса, он должен возвращать поставщик с помощью функции [**уиаретурнравелементпровидер**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="46d2e-121">If the server is implementing UI Automation, it should return a provider using the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>
-   <span data-ttu-id="46d2e-122">Если *двобжид* — [**OBJID \_ нативеом**](object-identifiers.md), то запрос предназначен для базовой объектной модели элемента управления.</span><span class="sxs-lookup"><span data-stu-id="46d2e-122">If *dwObjId* is [**OBJID\_NATIVEOM**](object-identifiers.md), the request is for the control's underlying object model.</span></span> <span data-ttu-id="46d2e-123">Если элемент управления поддерживает этот запрос, он должен вернуть соответствующий COM-интерфейс, вызвав функцию [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="46d2e-123">If the control supports this request, it should return an appropriate COM interface by calling the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>
-   <span data-ttu-id="46d2e-124">Если *двобжид* — [**OBJID \_ куерикласснамеидкс**](object-identifiers.md), то запрос предназначен для того, чтобы элемент управления определял себя как стандартный элемент управления Windows или обычный элемент управления, реализованный общей библиотекой элементов управления (ComCtrl.dll).</span><span class="sxs-lookup"><span data-stu-id="46d2e-124">If *dwObjId* is [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md), the request is for the control to identify itself as a standard Windows control or a common control implemented by the common control library (ComCtrl.dll).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46d2e-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46d2e-125">Return value</span></span>

<span data-ttu-id="46d2e-126">Если окну или элементу управления не нужно отвечать на это сообщение, оно должно передать сообщение функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ; в противном случае окно или элемент управления должны возвращать значение, соответствующее запросу, заданному параметром *двобжид*:</span><span class="sxs-lookup"><span data-stu-id="46d2e-126">If the window or control does not need to respond to this message, it should pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function; otherwise, the window or control should return a value that corresponds to the request specified by *dwObjId*:</span></span>

-   <span data-ttu-id="46d2e-127">Если окно или элемент управления реализует автоматизацию пользовательского интерфейса, окно или элемент управления должны возвращать значение, полученное при вызове функции [**уиаретурнравелементпровидер**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="46d2e-127">If the window or control implements UI Automation, the window or control should return the value obtained by a call to the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>
-   <span data-ttu-id="46d2e-128">Если *двобжид* — [**OBJID \_ нативеом**](object-identifiers.md) , а окно предоставляет собственную объектную модель, то Windows должна вернуть значение, полученное при вызове функции [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="46d2e-128">If *dwObjId* is [**OBJID\_NATIVEOM**](object-identifiers.md) and the window exposes a native Object Model, the windows should return the value obtained by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>
-   <span data-ttu-id="46d2e-129">Если *двобжид* — [**OBJID \_ Client**](object-identifiers.md) , а окно реализует [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), окно должно вернуть значение, полученное при вызове функции [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="46d2e-129">If *dwObjId* is [**OBJID\_CLIENT**](object-identifiers.md) and the window implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), the window should return the value obtained by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="46d2e-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46d2e-130">Remarks</span></span>

<span data-ttu-id="46d2e-131">Когда клиент вызывает [**акцессиблеобжектфромвиндов**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) или любую другую функцию **акцессиблеобжектфром**_X_ , которая получает интерфейс к объекту, Microsoft Active Accessibility отправляет сообщение **WM \_ GetObject** в соответствующую процедуру окна в соответствующем серверном приложении.</span><span class="sxs-lookup"><span data-stu-id="46d2e-131">When a client calls [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) or any of the other **AccessibleObjectFrom**_X_ functions that retrieve an interface to an object, Microsoft Active Accessibility sends the **WM\_GETOBJECT** message to the appropriate window procedure within the appropriate server application.</span></span> <span data-ttu-id="46d2e-132">При обработке **WM \_ GetObject** серверные приложения вызывают [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) и используют возвращаемое значение этой функции в качестве возвращаемого значения для сообщения.</span><span class="sxs-lookup"><span data-stu-id="46d2e-132">While processing **WM\_GETOBJECT**, server applications call [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) and use the return value of this function as the return value for the message.</span></span> <span data-ttu-id="46d2e-133">Microsoft Active Accessibility, в сочетании с библиотекой COM, выполняет соответствующий маршалирование и передает указатель интерфейса с сервера обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="46d2e-133">Microsoft Active Accessibility, in conjunction with the COM library, performs the appropriate marshaling and passes the interface pointer from the server back to the client.</span></span>

<span data-ttu-id="46d2e-134">Серверы не отвечают на **WM \_ GetObject** перед полной инициализацией объекта или после его начала.</span><span class="sxs-lookup"><span data-stu-id="46d2e-134">Servers do not respond to **WM\_GETOBJECT** before the object is fully initialized or after it begins to close down.</span></span> <span data-ttu-id="46d2e-135">Когда приложение создает новое окно, система отправляет [**\_ объект события \_ CREATE**](event-constants.md) для уведомления клиентов перед отправкой сообщения о [ \_ создании WM](../winmsg/wm-create.md) в процедуру окна приложения.</span><span class="sxs-lookup"><span data-stu-id="46d2e-135">When an application creates a new window, the system sends [**EVENT\_OBJECT\_CREATE**](event-constants.md) to notify clients before it sends the [WM\_CREATE](../winmsg/wm-create.md) message to the application's window procedure.</span></span> <span data-ttu-id="46d2e-136">Так как многие приложения используют приложение WM \_ Create для запуска процесса инициализации, серверы не реагируют на сообщение **WM \_ GetObject** до тех пор, пока не завершится обработка сообщения **WM \_ CREATE** .</span><span class="sxs-lookup"><span data-stu-id="46d2e-136">Because many applications use WM\_CREATE to start their initialization process, servers do not respond to the **WM\_GETOBJECT** message until finished processing the **WM\_CREATE** message.</span></span>

<span data-ttu-id="46d2e-137">Сервер использует **WM \_ GetObject** для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="46d2e-137">A server uses **WM\_GETOBJECT** to perform the following tasks:</span></span>

-   [<span data-ttu-id="46d2e-138">Создание новых объектов со специальными возможностями</span><span class="sxs-lookup"><span data-stu-id="46d2e-138">Create New Accessible Objects</span></span>](create-new-accessible-objects.md)
-   [<span data-ttu-id="46d2e-139">Повторное использование существующих указателей на объекты</span><span class="sxs-lookup"><span data-stu-id="46d2e-139">Reuse Existing Pointers to Objects</span></span>](reuse-existing-pointers-to-objects.md)
-   [<span data-ttu-id="46d2e-140">Создание новых интерфейсов для одного и того же объекта</span><span class="sxs-lookup"><span data-stu-id="46d2e-140">Create New Interfaces to the Same Object</span></span>](create-new-interfaces-to-the-same-object.md)

<span data-ttu-id="46d2e-141">Для клиентов это означает, что они могут получить разные указатели интерфейса для одного и того же элемента пользовательского интерфейса в зависимости от действия сервера.</span><span class="sxs-lookup"><span data-stu-id="46d2e-141">For clients, this means that they might receive distinct interface pointers for the same user interface element, depending on the server's action.</span></span> <span data-ttu-id="46d2e-142">Чтобы определить, указывают ли два указателя интерфейса на один и тот же элемент пользовательского интерфейса, клиенты сравнивают свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) объекта.</span><span class="sxs-lookup"><span data-stu-id="46d2e-142">To determine if two interface pointers point to the same user interface element, clients compare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties of the object.</span></span> <span data-ttu-id="46d2e-143">Сравнение указателей не работает.</span><span class="sxs-lookup"><span data-stu-id="46d2e-143">Comparing pointers does not work.</span></span>

## <a name="requirements"></a><span data-ttu-id="46d2e-144">Требования</span><span class="sxs-lookup"><span data-stu-id="46d2e-144">Requirements</span></span>



| <span data-ttu-id="46d2e-145">Требование</span><span class="sxs-lookup"><span data-stu-id="46d2e-145">Requirement</span></span> | <span data-ttu-id="46d2e-146">Значение</span><span class="sxs-lookup"><span data-stu-id="46d2e-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46d2e-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46d2e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="46d2e-148">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="46d2e-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="46d2e-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46d2e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="46d2e-150">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="46d2e-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="46d2e-151">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="46d2e-151">Redistributable</span></span><br/>          | <span data-ttu-id="46d2e-152">Active Accessibility 1,3 RDK в Windows NT 4,0 с пакетом обновления SP6 и более поздней версии и Windows 95</span><span class="sxs-lookup"><span data-stu-id="46d2e-152">Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95</span></span><br/>              |
| <span data-ttu-id="46d2e-153">Header</span><span class="sxs-lookup"><span data-stu-id="46d2e-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="46d2e-154"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46d2e-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46d2e-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46d2e-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d2e-156">Как работать с WM \_ GetObject</span><span class="sxs-lookup"><span data-stu-id="46d2e-156">How to Handle WM\_GETOBJECT</span></span>](how-to-handle-wm-getobject.md)
</dt> <dt>

[<span data-ttu-id="46d2e-157">Как \_ работает WM GetObject</span><span class="sxs-lookup"><span data-stu-id="46d2e-157">How WM\_GETOBJECT Works</span></span>](how-wm-getobject-works.md)
</dt> <dt>

[<span data-ttu-id="46d2e-158">**Функции lresultfromobject**</span><span class="sxs-lookup"><span data-stu-id="46d2e-158">**LresultFromObject**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

