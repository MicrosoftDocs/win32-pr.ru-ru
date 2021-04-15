---
description: Интерфейс ИтпартиЦипантевент содержит методы, которые извлекают описание событий участника.
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: Интерфейс ИтпартиЦипантевент (Конфприв. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac6e2b43a528bc041a71962e84b4e1be62152a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675633"
---
# <a name="itparticipantevent-interface"></a><span data-ttu-id="c1ffe-103">Интерфейс ИтпартиЦипантевент</span><span class="sxs-lookup"><span data-stu-id="c1ffe-103">ITParticipantEvent interface</span></span>

<span data-ttu-id="c1ffe-104">\[**ИтпартиЦипантевент** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-104">\[**ITParticipantEvent** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c1ffe-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="c1ffe-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c1ffe-106">Интерфейс **итпартиЦипантевент** содержит методы, которые извлекают описание событий участника.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-106">The **ITParticipantEvent** interface contains methods that retrieve the description of participant events.</span></span> <span data-ttu-id="c1ffe-107">Когда реализация метода [**иттапиевентнотификатион:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) в приложении указывает на [**\_ событие TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) , равное **\_ закрытому TE**, параметр *певент* метода является указателем **IDispatch** для интерфейса **итпартиЦипантевент** .</span><span class="sxs-lookup"><span data-stu-id="c1ffe-107">When the application's implementation of the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method indicates a [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) equal to **TE\_PRIVATE**, the method's *pEvent* parameter is an **IDispatch** pointer for the **ITParticipantEvent** interface.</span></span> <span data-ttu-id="c1ffe-108">Методы этого интерфейса можно использовать для получения сведений о произошедших изменениях участника.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-108">The methods of this interface can be used to retrieve information concerning a participant change that has occurred.</span></span>

> [!Note]  
> <span data-ttu-id="c1ffe-109">Необходимо вызвать метод [**иттапи::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) и задать маску фильтра событий, включающую **\_ закрытое событие TE** , чтобы включить прием событий участников.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-109">You must call the [**ITTAPI::put\_EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) method and set an event filter mask that includes the **TE\_PRIVATE** event to enable reception of participant events.</span></span> <span data-ttu-id="c1ffe-110">Если не вызвать **иттапи::p UT \_ EventFilter**, приложение не будет принимать никаких событий.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-110">If you do not call **ITTAPI::put\_EventFilter**, your application will not receive any events.</span></span> <span data-ttu-id="c1ffe-111">Дополнительные сведения см. в разделе Общие сведения о [событиях](events.md) .</span><span class="sxs-lookup"><span data-stu-id="c1ffe-111">For more information, see the [Events](events.md) overview.</span></span>

 

## <a name="members"></a><span data-ttu-id="c1ffe-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="c1ffe-112">Members</span></span>

<span data-ttu-id="c1ffe-113">Интерфейс **итпартиЦипантевент** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c1ffe-113">The **ITParticipantEvent** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c1ffe-114">**ИтпартиЦипантевент** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c1ffe-114">**ITParticipantEvent** also has these types of members:</span></span>

-   [<span data-ttu-id="c1ffe-115">Методы</span><span class="sxs-lookup"><span data-stu-id="c1ffe-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c1ffe-116">Методы</span><span class="sxs-lookup"><span data-stu-id="c1ffe-116">Methods</span></span>

<span data-ttu-id="c1ffe-117">Интерфейс **итпартиЦипантевент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-117">The **ITParticipantEvent** interface has these methods.</span></span>



| <span data-ttu-id="c1ffe-118">Метод</span><span class="sxs-lookup"><span data-stu-id="c1ffe-118">Method</span></span>                                                         | <span data-ttu-id="c1ffe-119">Описание</span><span class="sxs-lookup"><span data-stu-id="c1ffe-119">Description</span></span>                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1ffe-120">**получить \_ событие**</span><span class="sxs-lookup"><span data-stu-id="c1ffe-120">**get\_Event**</span></span>](itparticipantevent-get-event.md)             | <span data-ttu-id="c1ffe-121">Возвращает дескриптор [**события \_ участника**](participant-event.md) события.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-121">Gets the [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the event.</span></span><br/>                                                    |
| [<span data-ttu-id="c1ffe-122">**получить \_ участника**</span><span class="sxs-lookup"><span data-stu-id="c1ffe-122">**get\_Participant**</span></span>](itparticipantevent-get-participant.md) | <span data-ttu-id="c1ffe-123">Возвращает указатель на массив интерфейсов [**итпартиЦипант**](itparticipant.md) , представляющих участников, вовлеченных в событие.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-123">Gets a pointer to an array of [**ITParticipant**](itparticipant.md) interfaces representing the participants involved in the event.</span></span><br/> |
| [<span data-ttu-id="c1ffe-124">**получить \_ подпоток**</span><span class="sxs-lookup"><span data-stu-id="c1ffe-124">**get\_SubStream**</span></span>](itparticipantevent-get-substream.md)     | <span data-ttu-id="c1ffe-125">Возвращает указатель на массив интерфейсов [**итсубстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) , представляющих подпотоки, участвующие в событии.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-125">Gets a pointer to an array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces representing the substreams involved in the event.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="c1ffe-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c1ffe-126">Requirements</span></span>



| <span data-ttu-id="c1ffe-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c1ffe-127">Requirement</span></span> | <span data-ttu-id="c1ffe-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c1ffe-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1ffe-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="c1ffe-129">TAPI version</span></span><br/> | <span data-ttu-id="c1ffe-130">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="c1ffe-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c1ffe-131">Header</span><span class="sxs-lookup"><span data-stu-id="c1ffe-131">Header</span></span><br/>       | <dl> <span data-ttu-id="c1ffe-132"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1ffe-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="c1ffe-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c1ffe-133">Library</span></span><br/>      | <dl> <span data-ttu-id="c1ffe-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1ffe-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c1ffe-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c1ffe-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="c1ffe-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1ffe-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c1ffe-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1ffe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1ffe-138">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="c1ffe-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="c1ffe-139">**итсубстреам**</span><span class="sxs-lookup"><span data-stu-id="c1ffe-139">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[<span data-ttu-id="c1ffe-140">**иткаллинфо**</span><span class="sxs-lookup"><span data-stu-id="c1ffe-140">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="c1ffe-141">**\_событие участника**</span><span class="sxs-lookup"><span data-stu-id="c1ffe-141">**PARTICIPANT\_EVENT**</span></span>](participant-event.md)
</dt> <dt>

[<span data-ttu-id="c1ffe-142">**Иттапиевентнотификатион:: Event**</span><span class="sxs-lookup"><span data-stu-id="c1ffe-142">**ITTAPIEventNotification::Event**</span></span>](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[<span data-ttu-id="c1ffe-143">**\_событие TAPI**</span><span class="sxs-lookup"><span data-stu-id="c1ffe-143">**TAPI\_EVENT**</span></span>](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[<span data-ttu-id="c1ffe-144">Фрагмент кода регистрации событий</span><span class="sxs-lookup"><span data-stu-id="c1ffe-144">Register Events code snippet</span></span>](register-events.md)
</dt> </dl>

 

