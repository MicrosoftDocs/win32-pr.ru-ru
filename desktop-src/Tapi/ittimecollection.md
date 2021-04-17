---
description: Интерфейс Иттимеколлектион — это интерфейс, зависящий от поставщика, для объекта типа "объект" BLOB-объектов для Конференции по протоколу дескрипторов сеансов (SDP).
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: Интерфейс Иттимеколлектион (Сдпблб. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19ca297a26b0eac34396726e6145a24fba5a2ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685350"
---
# <a name="ittimecollection-interface"></a><span data-ttu-id="14a05-103">Интерфейс Иттимеколлектион</span><span class="sxs-lookup"><span data-stu-id="14a05-103">ITTimeCollection interface</span></span>

<span data-ttu-id="14a05-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="14a05-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="14a05-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="14a05-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="14a05-106">Интерфейс **иттимеколлектион** — это интерфейс, зависящий от поставщика, для объекта типа "объект" BLOB-объектов для Конференции по протоколу дескрипторов сеансов (SDP).</span><span class="sxs-lookup"><span data-stu-id="14a05-106">The **ITTimeCollection** interface is a provider-specific interface for the Session Descriptor Protocol (SDP) conference blob object.</span></span> <span data-ttu-id="14a05-107">Этот интерфейс обеспечивает доступ к [**иттиме**](ittime.md) интерфейсам по индексу, а также включает создание и удаление компонентов времени.</span><span class="sxs-lookup"><span data-stu-id="14a05-107">This interface allows access to [**ITTime**](ittime.md) interfaces by index, and also enable the creation and deletion of time components.</span></span> <span data-ttu-id="14a05-108">Метод [**итсдп:: Get \_ тимеколлектион**](itsdp-get-timecollection.md) создает интерфейс **иттимеколлектион** .</span><span class="sxs-lookup"><span data-stu-id="14a05-108">The [**ITSdp::get\_TimeCollection**](itsdp-get-timecollection.md) method creates the **ITTimeCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="14a05-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="14a05-109">Members</span></span>

<span data-ttu-id="14a05-110">Интерфейс **иттимеколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="14a05-110">The **ITTimeCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="14a05-111">**Иттимеколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="14a05-111">**ITTimeCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="14a05-112">Методы</span><span class="sxs-lookup"><span data-stu-id="14a05-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="14a05-113">Методы</span><span class="sxs-lookup"><span data-stu-id="14a05-113">Methods</span></span>

<span data-ttu-id="14a05-114">Интерфейс **иттимеколлектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="14a05-114">The **ITTimeCollection** interface has these methods.</span></span>



| <span data-ttu-id="14a05-115">Метод</span><span class="sxs-lookup"><span data-stu-id="14a05-115">Method</span></span>                                                           | <span data-ttu-id="14a05-116">Описание</span><span class="sxs-lookup"><span data-stu-id="14a05-116">Description</span></span>                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14a05-117">**Создания**</span><span class="sxs-lookup"><span data-stu-id="14a05-117">**Create**</span></span>](ittimecollection-create.md)                        | <span data-ttu-id="14a05-118">Создает компонент [**иттиме**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="14a05-118">Creates an [**ITTime**](ittime.md) component.</span></span><br/>                                                             |
| [<span data-ttu-id="14a05-119">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="14a05-119">**Delete**</span></span>](ittimecollection-delete.md)                        | <span data-ttu-id="14a05-120">Удаляет компонент [**иттиме**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="14a05-120">Deletes an [**ITTime**](ittime.md) component.</span></span><br/>                                                             |
| [<span data-ttu-id="14a05-121">**получить \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="14a05-121">**get\_\_NewEnum**</span></span>](ittimecollection-get--newenum.md)          | <span data-ttu-id="14a05-122">Возвращает перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="14a05-122">Returns an enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="14a05-123">**получить \_ число**</span><span class="sxs-lookup"><span data-stu-id="14a05-123">**get\_Count**</span></span>](ittimecollection-get-count.md)                 | <span data-ttu-id="14a05-124">Возвращает число элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="14a05-124">Gets number of items in collection.</span></span><br/>                                                                        |
| [<span data-ttu-id="14a05-125">**получить \_ енумератиониф**</span><span class="sxs-lookup"><span data-stu-id="14a05-125">**get\_EnumerationIf**</span></span>](ittimecollection-get-enumerationif.md) | <span data-ttu-id="14a05-126">Возвращает интерфейс перечисления [**иенумтиме**](ienumtime.md) , перечисляющий [**иттиме**](ittime.md).</span><span class="sxs-lookup"><span data-stu-id="14a05-126">Returns the [**IEnumTime**](ienumtime.md) enumeration interface that enumerates [**ITTime**](ittime.md).</span></span><br/> |
| [<span data-ttu-id="14a05-127">**получить \_ элемент**</span><span class="sxs-lookup"><span data-stu-id="14a05-127">**get\_Item**</span></span>](ittimecollection-get-item.md)                   | <span data-ttu-id="14a05-128">При наличии индекса Возвращает элемент в коллекции.</span><span class="sxs-lookup"><span data-stu-id="14a05-128">Given an index, returns an item in the collection.</span></span><br/>                                                         |



 

## <a name="requirements"></a><span data-ttu-id="14a05-129">Требования</span><span class="sxs-lookup"><span data-stu-id="14a05-129">Requirements</span></span>



| <span data-ttu-id="14a05-130">Требование</span><span class="sxs-lookup"><span data-stu-id="14a05-130">Requirement</span></span> | <span data-ttu-id="14a05-131">Значение</span><span class="sxs-lookup"><span data-stu-id="14a05-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14a05-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="14a05-132">TAPI version</span></span><br/> | <span data-ttu-id="14a05-133">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="14a05-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="14a05-134">Header</span><span class="sxs-lookup"><span data-stu-id="14a05-134">Header</span></span><br/>       | <dl> <span data-ttu-id="14a05-135"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="14a05-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="14a05-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="14a05-136">Library</span></span><br/>      | <dl> <span data-ttu-id="14a05-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14a05-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="14a05-138">DLL</span><span class="sxs-lookup"><span data-stu-id="14a05-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="14a05-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14a05-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

