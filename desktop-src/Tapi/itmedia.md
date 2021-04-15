---
description: Интерфейс Итмедиа представляет собой представление мультимедиа в протоколе дескриптора сеанса (см. RFC 2327).
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: Интерфейс Итмедиа (Сдпблб. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd00d7eab685fe99b089556bcdb0ed2bf6329df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675777"
---
# <a name="itmedia-interface"></a><span data-ttu-id="ecb2a-103">Интерфейс Итмедиа</span><span class="sxs-lookup"><span data-stu-id="ecb2a-103">ITMedia interface</span></span>

<span data-ttu-id="ecb2a-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="ecb2a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ecb2a-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="ecb2a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ecb2a-106">Интерфейс **итмедиа** представляет собой представление мультимедиа в протоколе дескриптора сеанса (см. RFC 2327).</span><span class="sxs-lookup"><span data-stu-id="ecb2a-106">The **ITMedia** interface is a representation of media in a Session Descriptor Protocol (SDP, see RFC 2327).</span></span> <span data-ttu-id="ecb2a-107">Этот интерфейс экспортирует методы для получения и задания основных свойств носителя, таких как тип.</span><span class="sxs-lookup"><span data-stu-id="ecb2a-107">This interface exports methods to get and set basic media properties, such as type.</span></span> <span data-ttu-id="ecb2a-108">Методы [**итмедиаколлектион:: Get \_ Item**](itmediacollection-get-item.md) и [**итмедиаколлектион:: Create**](itmediacollection-create.md) создают интерфейс **итмедиа** .</span><span class="sxs-lookup"><span data-stu-id="ecb2a-108">The [**ITMediaCollection::get\_Item**](itmediacollection-get-item.md) and [**ITMediaCollection::Create**](itmediacollection-create.md) methods create the **ITMedia** interface.</span></span>

## <a name="members"></a><span data-ttu-id="ecb2a-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="ecb2a-109">Members</span></span>

<span data-ttu-id="ecb2a-110">Интерфейс **итмедиа** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="ecb2a-110">The **ITMedia** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="ecb2a-111">**Итмедиа** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ecb2a-111">**ITMedia** also has these types of members:</span></span>

-   [<span data-ttu-id="ecb2a-112">Методы</span><span class="sxs-lookup"><span data-stu-id="ecb2a-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ecb2a-113">Методы</span><span class="sxs-lookup"><span data-stu-id="ecb2a-113">Methods</span></span>

<span data-ttu-id="ecb2a-114">Интерфейс **итмедиа** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ecb2a-114">The **ITMedia** interface has these methods.</span></span>



| <span data-ttu-id="ecb2a-115">Метод</span><span class="sxs-lookup"><span data-stu-id="ecb2a-115">Method</span></span>                                                          | <span data-ttu-id="ecb2a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ecb2a-116">Description</span></span>                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ecb2a-117">**получить \_ форматкодес**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-117">**get\_FormatCodes**</span></span>](itmedia-get-formatcodes.md)             | <span data-ttu-id="ecb2a-118">Возвращает список кодов формата полезных данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ecb2a-118">Gets the list of media payload format codes.</span></span><br/>                                          |
| [<span data-ttu-id="ecb2a-119">**получить \_ MediaName**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-119">**get\_MediaName**</span></span>](itmedia-get-medianame.md)                 | <span data-ttu-id="ecb2a-120">Возвращает имя носителя.</span><span class="sxs-lookup"><span data-stu-id="ecb2a-120">Gets the media name.</span></span><br/>                                                                  |
| [<span data-ttu-id="ecb2a-121">**получить \_ медиатитле**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-121">**get\_MediaTitle**</span></span>](itmedia-get-mediatitle.md)               | <span data-ttu-id="ecb2a-122">Возвращает заголовок носителя.</span><span class="sxs-lookup"><span data-stu-id="ecb2a-122">Gets the media title.</span></span><br/>                                                                 |
| [<span data-ttu-id="ecb2a-123">**получить \_ нумпортс**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-123">**get\_NumPorts**</span></span>](itmedia-get-numports.md)                   | <span data-ttu-id="ecb2a-124">Возвращает количество портов, необходимых для сеанса.</span><span class="sxs-lookup"><span data-stu-id="ecb2a-124">Gets the number of ports needed for the session.</span></span><br/>                                      |
| [<span data-ttu-id="ecb2a-125">**получить \_ стартпорт**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-125">**get\_StartPort**</span></span>](itmedia-get-startport.md)                 | <span data-ttu-id="ecb2a-126">Возвращает 16-битное значение порта для первого порта.</span><span class="sxs-lookup"><span data-stu-id="ecb2a-126">Gets the 16-bit port value for the first port.</span></span><br/>                                        |
| [<span data-ttu-id="ecb2a-127">**получить \_ транспортпротокол**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-127">**get\_TransportProtocol**</span></span>](itmedia-get-transportprotocol.md) | <span data-ttu-id="ecb2a-128">Возвращает транспортный протокол.</span><span class="sxs-lookup"><span data-stu-id="ecb2a-128">Gets the transport protocol.</span></span><br/>                                                          |
| [<span data-ttu-id="ecb2a-129">**разместить \_ форматкодес**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-129">**put\_FormatCodes**</span></span>](itmedia-put-formatcodes.md)             | <span data-ttu-id="ecb2a-130">Задает список кодов формата полезных данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ecb2a-130">Sets the list of media payload format codes.</span></span><br/>                                          |
| [<span data-ttu-id="ecb2a-131">**разместить \_ MediaName**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-131">**put\_MediaName**</span></span>](itmedia-put-medianame.md)                 | <span data-ttu-id="ecb2a-132">Задает имя носителя.</span><span class="sxs-lookup"><span data-stu-id="ecb2a-132">Sets the media name.</span></span><br/>                                                                  |
| [<span data-ttu-id="ecb2a-133">**разместить \_ медиатитле**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-133">**put\_MediaTitle**</span></span>](itmedia-put-mediatitle.md)               | <span data-ttu-id="ecb2a-134">Задает заголовок носителя.</span><span class="sxs-lookup"><span data-stu-id="ecb2a-134">Sets the media title.</span></span><br/>                                                                 |
| [<span data-ttu-id="ecb2a-135">**разместить \_ транспортпротокол**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-135">**put\_TransportProtocol**</span></span>](itmedia-put-transportprotocol.md) | <span data-ttu-id="ecb2a-136">Задает транспортный протокол.</span><span class="sxs-lookup"><span data-stu-id="ecb2a-136">Sets the transport protocol.</span></span><br/>                                                          |
| [<span data-ttu-id="ecb2a-137">**сетпортинфо**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-137">**SetPortInfo**</span></span>](itmedia-setportinfo.md)                      | <span data-ttu-id="ecb2a-138">Задает 16-битное значение порта для первого порта и число портов, необходимых для сеанса.</span><span class="sxs-lookup"><span data-stu-id="ecb2a-138">Sets the 16-bit port value for the first port and number of ports needed for session.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ecb2a-139">Требования</span><span class="sxs-lookup"><span data-stu-id="ecb2a-139">Requirements</span></span>



| <span data-ttu-id="ecb2a-140">Требование</span><span class="sxs-lookup"><span data-stu-id="ecb2a-140">Requirement</span></span> | <span data-ttu-id="ecb2a-141">Значение</span><span class="sxs-lookup"><span data-stu-id="ecb2a-141">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb2a-142">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="ecb2a-142">TAPI version</span></span><br/> | <span data-ttu-id="ecb2a-143">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ecb2a-143">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ecb2a-144">Header</span><span class="sxs-lookup"><span data-stu-id="ecb2a-144">Header</span></span><br/>       | <dl> <span data-ttu-id="ecb2a-145"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecb2a-145"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ecb2a-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ecb2a-146">Library</span></span><br/>      | <dl> <span data-ttu-id="ecb2a-147"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecb2a-147"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ecb2a-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ecb2a-148">DLL</span></span><br/>          | <dl> <span data-ttu-id="ecb2a-149"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecb2a-149"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb2a-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecb2a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb2a-151">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-151">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="ecb2a-152">**итмедиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-152">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> <dt>

[<span data-ttu-id="ecb2a-153">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-153">**ITSDP**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="ecb2a-154">**иттиме**</span><span class="sxs-lookup"><span data-stu-id="ecb2a-154">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

