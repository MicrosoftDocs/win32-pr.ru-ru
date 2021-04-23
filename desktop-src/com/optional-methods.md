---
title: Необязательные методы
description: Необязательные методы
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904aad26ecfba6396c9911b247443f9a956bca7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134615"
---
# <a name="optional-methods"></a><span data-ttu-id="5d4ed-103">Необязательные методы</span><span class="sxs-lookup"><span data-stu-id="5d4ed-103">Optional Methods</span></span>

<span data-ttu-id="5d4ed-104">Компонент OLE может реализовать интерфейс, не реализуя всю семантику каждого метода в интерфейсе, вместо этого возвращая E \_ нотимпл или S \_ ОК соответственно.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-104">An OLE component can implement an interface without implementing all the semantics of every method in the interface, instead returning E\_NOTIMPL or S\_OK as appropriate.</span></span> <span data-ttu-id="5d4ed-105">В следующей таблице описаны методы, которые не требуется реализовать контейнеру элемента управления ActiveX (т. е. контейнер элемента управления может возвращать E \_ нотимпл).</span><span class="sxs-lookup"><span data-stu-id="5d4ed-105">The following table describes those methods that an ActiveX control container is not required to implement (i.e. the control container can return E\_NOTIMPL).</span></span>

<span data-ttu-id="5d4ed-106">В таблице ниже описываются необязательные методы. Обратите внимание, что метод по-прежнему должен существовать, но может просто возвращать E \_ нотимпл вместо реализации реальной семантики.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-106">The table below describes optional methods; note that the method must still exist, but can simply return E\_NOTIMPL instead of implementing real semantics.</span></span> <span data-ttu-id="5d4ed-107">Обратите внимание, что любой метод из обязательного интерфейса, который не указан ниже, должен считаться обязательным и не может возвращать E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-107">Note that any method from a mandatory interface that is not listed below must be considered mandatory and may not return E\_NOTIMPL.</span></span>

## <a name="ioleclientsite"></a><span data-ttu-id="5d4ed-108">иолеклиентсите</span><span class="sxs-lookup"><span data-stu-id="5d4ed-108">IOleClientSite</span></span>



| <span data-ttu-id="5d4ed-109">Метод</span><span class="sxs-lookup"><span data-stu-id="5d4ed-109">Method</span></span>                                                     | <span data-ttu-id="5d4ed-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d4ed-110">Comments</span></span>                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d4ed-111">**савеобжект**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-111">**SaveObject**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | <span data-ttu-id="5d4ed-112">Требуется для успешной поддержки сохраняемости.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-112">Necessary for persistence to be successfully supported.</span></span><br/>                                       |
| [<span data-ttu-id="5d4ed-113">**Моникер**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-113">**GetMoniker**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | <span data-ttu-id="5d4ed-114">Требуется только в том случае, если контейнер поддерживает связывание с элементами управления в собственной форме или документе.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-114">Necessary only if the container supports linking to controls within its own form or document.</span></span><br/> |



 

## <a name="ioleinplacesite"></a><span data-ttu-id="5d4ed-115">иолеинплацесите</span><span class="sxs-lookup"><span data-stu-id="5d4ed-115">IOleInPlaceSite</span></span>



| <span data-ttu-id="5d4ed-116">Метод</span><span class="sxs-lookup"><span data-stu-id="5d4ed-116">Method</span></span>                                                                     | <span data-ttu-id="5d4ed-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d4ed-117">Comments</span></span>                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="5d4ed-118">**контекстсенситивехелп**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-118">**ContextSensitiveHelp**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | <span data-ttu-id="5d4ed-119">Необязательно</span><span class="sxs-lookup"><span data-stu-id="5d4ed-119">Optional</span></span><br/>                                      |
| [<span data-ttu-id="5d4ed-120">**Scroll**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-120">**Scroll**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | <span data-ttu-id="5d4ed-121">Может возвращать \_ значение false без действия.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-121">May return S\_FALSE with no action.</span></span><br/>           |
| [<span data-ttu-id="5d4ed-122">**дискардундостате**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-122">**DiscardUndoState**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | <span data-ttu-id="5d4ed-123">Может вернуть S \_ ОК без действий.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-123">Can return S\_OK with no action.</span></span><br/>              |
| [<span data-ttu-id="5d4ed-124">**деактиватеандундо**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-124">**DeactivateAndUndo**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | <span data-ttu-id="5d4ed-125">Деактивация является обязательной. Undo является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-125">Deactivation is mandatory; Undo is optional.</span></span> <br/> |



 

## <a name="iolecontrolsite"></a><span data-ttu-id="5d4ed-126">IOleControlSite</span><span class="sxs-lookup"><span data-stu-id="5d4ed-126">IOleControlSite</span></span>



| <span data-ttu-id="5d4ed-127">Метод</span><span class="sxs-lookup"><span data-stu-id="5d4ed-127">Method</span></span>                                                                          | <span data-ttu-id="5d4ed-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d4ed-128">Comments</span></span>                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d4ed-129">**жетекстендедконтрол**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-129">**GetExtendedControl**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | <span data-ttu-id="5d4ed-130">Необходим для контейнеров, поддерживающих расширенные элементы управления.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-130">Necessary for containers that support extended controls.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="5d4ed-131">**шовпропертифраме**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-131">**ShowPropertyFrame**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | <span data-ttu-id="5d4ed-132">Необходим для контейнеров, которые хотят включить собственные страницы свойств для работы с расширенными свойствами элемента управления в дополнение к элементам, предоставленным элементом управления.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-132">Necessary for containers that wish to include their own property pages to handle extended control properties in addition to those provided by a control.</span></span><br/> |
| [<span data-ttu-id="5d4ed-133">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-133">**TranslateAccelerator**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | <span data-ttu-id="5d4ed-134">Может возвращать \_ значение false без действия.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-134">May return S\_FALSE with no action.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="5d4ed-135">**локкинплацеактиве**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-135">**LockInPlaceActive**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | <span data-ttu-id="5d4ed-136">Необязательно</span><span class="sxs-lookup"><span data-stu-id="5d4ed-136">Optional</span></span><br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a><span data-ttu-id="5d4ed-137">IDispatch (свойства окружения)</span><span class="sxs-lookup"><span data-stu-id="5d4ed-137">IDispatch (Ambient properties)</span></span>



| <span data-ttu-id="5d4ed-138">Метод</span><span class="sxs-lookup"><span data-stu-id="5d4ed-138">Method</span></span>                      | <span data-ttu-id="5d4ed-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d4ed-139">Comments</span></span>                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5d4ed-140">жеттипеинфокаунт</span><span class="sxs-lookup"><span data-stu-id="5d4ed-140">GetTypeInfoCount</span></span><br/> | <span data-ttu-id="5d4ed-141">Необходим для контейнеров, поддерживающих нестандартные свойства окружения.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-141">Necessary for containers that support non-standard ambient properties.</span></span><br/> |
| <span data-ttu-id="5d4ed-142">GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="5d4ed-142">GetTypeInfo</span></span><br/>      | <span data-ttu-id="5d4ed-143">Необходим для контейнеров, поддерживающих нестандартные свойства окружения.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-143">Necessary for containers that support non-standard ambient properties.</span></span><br/> |
| <span data-ttu-id="5d4ed-144">GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="5d4ed-144">GetIDsOfNames</span></span><br/>    | <span data-ttu-id="5d4ed-145">Необходим для контейнеров, поддерживающих нестандартные свойства окружения.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-145">Necessary for containers that support non-standard ambient properties.</span></span><br/> |



 

## <a name="idispatch-event-sink"></a><span data-ttu-id="5d4ed-146">IDispatch (приемник событий)</span><span class="sxs-lookup"><span data-stu-id="5d4ed-146">IDispatch (Event sink)</span></span>



| <span data-ttu-id="5d4ed-147">Метод</span><span class="sxs-lookup"><span data-stu-id="5d4ed-147">Method</span></span>                      | <span data-ttu-id="5d4ed-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d4ed-148">Comments</span></span>                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d4ed-149">жеттипеинфокаунт</span><span class="sxs-lookup"><span data-stu-id="5d4ed-149">GetTypeInfoCount</span></span><br/> | <span data-ttu-id="5d4ed-150">Элемент управления знает сведения о его собственном типе, поэтому его не нужно вызывать.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-150">The control knows its own type information, so it has no need to call this.</span></span><br/> |
| <span data-ttu-id="5d4ed-151">GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="5d4ed-151">GetTypeInfo</span></span><br/>      | <span data-ttu-id="5d4ed-152">Элемент управления знает сведения о его собственном типе, поэтому его не нужно вызывать.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-152">The control knows its own type information, so it has no need to call this.</span></span><br/> |
| <span data-ttu-id="5d4ed-153">GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="5d4ed-153">GetIDsOfNames</span></span><br/>    | <span data-ttu-id="5d4ed-154">Элемент управления знает сведения о его собственном типе, поэтому его не нужно вызывать.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-154">The control knows its own type information, so it has no need to call this.</span></span><br/> |



 

## <a name="ioleinplaceframe"></a><span data-ttu-id="5d4ed-155">иолеинплацефраме</span><span class="sxs-lookup"><span data-stu-id="5d4ed-155">IOleInPlaceFrame</span></span>



| <span data-ttu-id="5d4ed-156">Метод</span><span class="sxs-lookup"><span data-stu-id="5d4ed-156">Method</span></span>                                                                           | <span data-ttu-id="5d4ed-157">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d4ed-157">Comments</span></span>                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="5d4ed-158">**контекстсенситивехелп**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-158">**ContextSensitiveHelp**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [<span data-ttu-id="5d4ed-159">**Награница**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-159">**GetBorder**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | <span data-ttu-id="5d4ed-160">Требуется для контейнеров с пользовательским интерфейсом панели инструментов (это необязательно)</span><span class="sxs-lookup"><span data-stu-id="5d4ed-160">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="5d4ed-161">**рекуестбордерспаце**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-161">**RequestBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | <span data-ttu-id="5d4ed-162">Требуется для контейнеров с пользовательским интерфейсом панели инструментов (это необязательно)</span><span class="sxs-lookup"><span data-stu-id="5d4ed-162">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="5d4ed-163">**сетбордерспаце**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-163">**SetBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | <span data-ttu-id="5d4ed-164">Требуется для контейнеров с пользовательским интерфейсом панели инструментов (это необязательно)</span><span class="sxs-lookup"><span data-stu-id="5d4ed-164">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="5d4ed-165">**инсертменус**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-165">**InsertMenus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | <span data-ttu-id="5d4ed-166">Требуется для контейнеров с пользовательским интерфейсом меню (это необязательно)</span><span class="sxs-lookup"><span data-stu-id="5d4ed-166">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="5d4ed-167">**сетмену**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-167">**SetMenu**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | <span data-ttu-id="5d4ed-168">Требуется для контейнеров с пользовательским интерфейсом меню (это необязательно)</span><span class="sxs-lookup"><span data-stu-id="5d4ed-168">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="5d4ed-169">**ремовеменус**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-169">**RemoveMenus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | <span data-ttu-id="5d4ed-170">Требуется для контейнеров с пользовательским интерфейсом меню (это необязательно)</span><span class="sxs-lookup"><span data-stu-id="5d4ed-170">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="5d4ed-171">**сетстатустекст**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-171">**SetStatusText**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | <span data-ttu-id="5d4ed-172">Требуется только для контейнеров, имеющих строку состояния</span><span class="sxs-lookup"><span data-stu-id="5d4ed-172">Necessary only for containers that have a status line</span></span><br/>        |
| [<span data-ttu-id="5d4ed-173">**енаблемоделесс**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-173">**EnableModeless**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | <span data-ttu-id="5d4ed-174">Необязательно</span><span class="sxs-lookup"><span data-stu-id="5d4ed-174">Optional</span></span><br/>                                                     |
| [<span data-ttu-id="5d4ed-175">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-175">**TranslateAccelerator**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | <span data-ttu-id="5d4ed-176">Необязательно</span><span class="sxs-lookup"><span data-stu-id="5d4ed-176">Optional</span></span><br/>                                                     |



 

## <a name="iolecontainer"></a><span data-ttu-id="5d4ed-177">иолеконтаинер</span><span class="sxs-lookup"><span data-stu-id="5d4ed-177">IOleContainer</span></span>



| <span data-ttu-id="5d4ed-178">Метод</span><span class="sxs-lookup"><span data-stu-id="5d4ed-178">Method</span></span>                                                                    | <span data-ttu-id="5d4ed-179">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d4ed-179">Comments</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d4ed-180">**парседисплайнаме**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-180">**ParseDisplayName**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | <span data-ttu-id="5d4ed-181">Только если связывание с элементами управления или другими внедрениями в контейнере поддерживается, так как это необходимо для привязки моникера.</span><span class="sxs-lookup"><span data-stu-id="5d4ed-181">Only if linking to controls or other embeddings in the container is supported, as this is necessary for moniker binding.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="5d4ed-182">**локкконтаинер**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-182">**LockContainer**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | <span data-ttu-id="5d4ed-183">Как для Парседисплайнаме</span><span class="sxs-lookup"><span data-stu-id="5d4ed-183">As for ParseDisplayName</span></span><br/>                                                                                                                                                                                                                   |
| [<span data-ttu-id="5d4ed-184">**енумобжектс**</span><span class="sxs-lookup"><span data-stu-id="5d4ed-184">**EnumObjects**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | <span data-ttu-id="5d4ed-185">Возвращает все элементы управления ActiveX через перечислитель с [**иенумункновн**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), но не обязательно все объекты (поскольку нет никакой гарантии, что все объекты являются элементами управления ActiveX; некоторые могут быть обычными элементами управления Windows).</span><span class="sxs-lookup"><span data-stu-id="5d4ed-185">Returns all ActiveX controls through an enumerator with [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), but not necessarily all objects (because there's no guarantee that all objects are ActiveX controls; some may be regular Windows controls).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5d4ed-186">См. также</span><span class="sxs-lookup"><span data-stu-id="5d4ed-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d4ed-187">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="5d4ed-187">Containers</span></span>](containers.md)
</dt> </dl>

 

