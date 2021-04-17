---
description: Интерфейс Итмедиаколлектион предоставляет доступ к набору сведений о файлах мультимедиа в описании конференции SDP (RFC 2327).
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: Интерфейс Итмедиаколлектион (Сдпблб. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21305e1d1729437b53c380b7712feee3827b3ba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685078"
---
# <a name="itmediacollection-interface"></a><span data-ttu-id="8b761-103">Интерфейс Итмедиаколлектион</span><span class="sxs-lookup"><span data-stu-id="8b761-103">ITMediaCollection interface</span></span>

<span data-ttu-id="8b761-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="8b761-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8b761-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="8b761-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8b761-106">Интерфейс **итмедиаколлектион** предоставляет доступ к набору сведений о файлах мультимедиа в описании конференции SDP (RFC 2327).</span><span class="sxs-lookup"><span data-stu-id="8b761-106">The **ITMediaCollection** interface provides access to the set of media information in an SDP (RFC 2327) conference description.</span></span> <span data-ttu-id="8b761-107">Каждое описание носителя в SDP описывается интерфейсом [**итмедиа**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="8b761-107">Each Media description in the SDP is described by an [**ITMedia**](itmedia.md) interface.</span></span> <span data-ttu-id="8b761-108">**Итмедиаколлектион** позволяет манипулировать сведениями о **итмедиа** для SDP, включая:</span><span class="sxs-lookup"><span data-stu-id="8b761-108">**ITMediaCollection** allows manipulation of the set of **ITMedia** information for the SDP, including:</span></span>

-   <span data-ttu-id="8b761-109">Разрешает доступ к носителю по индексу.</span><span class="sxs-lookup"><span data-stu-id="8b761-109">Allows media access by index.</span></span>
-   <span data-ttu-id="8b761-110">Включает создание и удаление носителей.</span><span class="sxs-lookup"><span data-stu-id="8b761-110">Enables creation and deletion of media.</span></span>

<span data-ttu-id="8b761-111">Метод [**итсдп:: Get \_ медиаколлектион**](itsdp-get-mediacollection.md) создает интерфейс **итмедиаколлектион** .</span><span class="sxs-lookup"><span data-stu-id="8b761-111">The [**ITSdp::get\_MediaCollection**](itsdp-get-mediacollection.md) method creates the **ITMediaCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="8b761-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="8b761-112">Members</span></span>

<span data-ttu-id="8b761-113">Интерфейс **итмедиаколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="8b761-113">The **ITMediaCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8b761-114">**Итмедиаколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8b761-114">**ITMediaCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="8b761-115">Методы</span><span class="sxs-lookup"><span data-stu-id="8b761-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8b761-116">Методы</span><span class="sxs-lookup"><span data-stu-id="8b761-116">Methods</span></span>

<span data-ttu-id="8b761-117">Интерфейс **итмедиаколлектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8b761-117">The **ITMediaCollection** interface has these methods.</span></span>



| <span data-ttu-id="8b761-118">Метод</span><span class="sxs-lookup"><span data-stu-id="8b761-118">Method</span></span>                                                            | <span data-ttu-id="8b761-119">Описание</span><span class="sxs-lookup"><span data-stu-id="8b761-119">Description</span></span>                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="8b761-120">**Создания**</span><span class="sxs-lookup"><span data-stu-id="8b761-120">**Create**</span></span>](itmediacollection-create.md)                        | <span data-ttu-id="8b761-121">Создает новый носитель со свойствами по умолчанию и возвращает его.</span><span class="sxs-lookup"><span data-stu-id="8b761-121">Creates a new media with default properties and returns it.</span></span><br/> |
| [<span data-ttu-id="8b761-122">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="8b761-122">**Delete**</span></span>](itmediacollection-delete.md)                        | <span data-ttu-id="8b761-123">Удаляет носитель, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="8b761-123">Deletes the media corresponding to the specified index.</span></span><br/>     |
| [<span data-ttu-id="8b761-124">**получить \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="8b761-124">**get\_\_NewEnum**</span></span>](itmediacollection-get--newenum.md)          | <span data-ttu-id="8b761-125">Возвращает перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="8b761-125">Returns an enumerator for the collection.</span></span><br/>                   |
| [<span data-ttu-id="8b761-126">**получить \_ число**</span><span class="sxs-lookup"><span data-stu-id="8b761-126">**get\_Count**</span></span>](itmediacollection-get-count.md)                 | <span data-ttu-id="8b761-127">Возвращает количество носителей в сеансе.</span><span class="sxs-lookup"><span data-stu-id="8b761-127">Gets the number of media in the session.</span></span><br/>                    |
| [<span data-ttu-id="8b761-128">**получить \_ енумератиониф**</span><span class="sxs-lookup"><span data-stu-id="8b761-128">**get\_EnumerationIf**</span></span>](itmediacollection-get-enumerationif.md) | <span data-ttu-id="8b761-129">Возвращает указатель на интерфейс перечисления.</span><span class="sxs-lookup"><span data-stu-id="8b761-129">Gets pointer to enumeration interface.</span></span><br/>                      |
| [<span data-ttu-id="8b761-130">**получить \_ элемент**</span><span class="sxs-lookup"><span data-stu-id="8b761-130">**get\_Item**</span></span>](itmediacollection-get-item.md)                   | <span data-ttu-id="8b761-131">Возвращает носитель, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="8b761-131">Returns the media corresponding to the specified index.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="8b761-132">Требования</span><span class="sxs-lookup"><span data-stu-id="8b761-132">Requirements</span></span>



| <span data-ttu-id="8b761-133">Требование</span><span class="sxs-lookup"><span data-stu-id="8b761-133">Requirement</span></span> | <span data-ttu-id="8b761-134">Значение</span><span class="sxs-lookup"><span data-stu-id="8b761-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b761-135">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8b761-135">TAPI version</span></span><br/> | <span data-ttu-id="8b761-136">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8b761-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8b761-137">Header</span><span class="sxs-lookup"><span data-stu-id="8b761-137">Header</span></span><br/>       | <dl> <span data-ttu-id="8b761-138"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b761-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b761-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8b761-139">Library</span></span><br/>      | <dl> <span data-ttu-id="8b761-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b761-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8b761-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8b761-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="8b761-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b761-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

