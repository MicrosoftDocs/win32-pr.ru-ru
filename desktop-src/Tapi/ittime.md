---
description: Интерфейс Иттиме представляет собой интерфейс, зависящий от поставщика, для объекта "объект большого двоичного объекта" в службе протокола дескрипторов сеансов (SDP).
ms.assetid: 24d33259-dcbe-47e4-9c71-fcc25f6e9a76
title: Интерфейс Иттиме (Сдпблб. h)
ms.topic: interface
ms.date: 05/31/2018
ms.openlocfilehash: 964fa197318d8cbe9614beb97c5bea0db94f242b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675278"
---
# <a name="ittime-interface"></a><span data-ttu-id="8e296-103">Интерфейс Иттиме</span><span class="sxs-lookup"><span data-stu-id="8e296-103">ITTime interface</span></span>

<span data-ttu-id="8e296-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="8e296-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8e296-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="8e296-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8e296-106">Интерфейс **иттиме** представляет собой интерфейс, зависящий от поставщика, для объекта "объект большого двоичного объекта" в службе протокола дескрипторов сеансов (SDP).</span><span class="sxs-lookup"><span data-stu-id="8e296-106">The **ITTime** interface is a provider-specific interface for a Session Descriptor Protocol (SDP) conference blob object.</span></span> <span data-ttu-id="8e296-107">Он предоставляет доступ к набору времени активации для сеанса.</span><span class="sxs-lookup"><span data-stu-id="8e296-107">It provides access to a set of activation times for the session.</span></span> <span data-ttu-id="8e296-108">Методы [**иенумтиме:: Next**](ienumtime-next.md) и [**Иттимеколлектион:: Create**](ittimecollection-create.md) создают интерфейс **иттиме** .</span><span class="sxs-lookup"><span data-stu-id="8e296-108">The [**IEnumTime::Next**](ienumtime-next.md) and [**ITTimeCollection::Create**](ittimecollection-create.md) methods create the **ITTime** interface.</span></span>

## <a name="members"></a><span data-ttu-id="8e296-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="8e296-109">Members</span></span>

<span data-ttu-id="8e296-110">Интерфейс **иттиме** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="8e296-110">The **ITTime** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8e296-111">**Иттиме** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8e296-111">**ITTime** also has these types of members:</span></span>

-   [<span data-ttu-id="8e296-112">Методы</span><span class="sxs-lookup"><span data-stu-id="8e296-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8e296-113">Методы</span><span class="sxs-lookup"><span data-stu-id="8e296-113">Methods</span></span>

<span data-ttu-id="8e296-114">Интерфейс **иттиме** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8e296-114">The **ITTime** interface has these methods.</span></span>



| <span data-ttu-id="8e296-115">Метод</span><span class="sxs-lookup"><span data-stu-id="8e296-115">Method</span></span>                                         | <span data-ttu-id="8e296-116">Описание</span><span class="sxs-lookup"><span data-stu-id="8e296-116">Description</span></span>                                                                 |
|:-----------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="8e296-117">**получение \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="8e296-117">**get\_StartTime**</span></span>](ittime-get-starttime.md) | <span data-ttu-id="8e296-118">Возвращает значение времени начала 32-разрядного NTP (сетевой протокол времени).</span><span class="sxs-lookup"><span data-stu-id="8e296-118">Gets the 32-bit NTP (Network Time Protocol) starting time value.</span></span><br/> |
| [<span data-ttu-id="8e296-119">**получить \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="8e296-119">**get\_StopTime**</span></span>](ittime-get-stoptime.md)   | <span data-ttu-id="8e296-120">Возвращает значение времени окончания NTP.</span><span class="sxs-lookup"><span data-stu-id="8e296-120">Gets the NTP ending time value.</span></span><br/>                                  |
| [<span data-ttu-id="8e296-121">**Добавление \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="8e296-121">**put\_StartTime**</span></span>](ittime-put-starttime.md) | <span data-ttu-id="8e296-122">Задает 32-разрядное значение времени начала NTP.</span><span class="sxs-lookup"><span data-stu-id="8e296-122">Sets the 32-bit NTP starting time value.</span></span><br/>                         |
| [<span data-ttu-id="8e296-123">**разместить \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="8e296-123">**put\_StopTime**</span></span>](ittime-put-stoptime.md)   | <span data-ttu-id="8e296-124">Задает значение времени окончания NTP.</span><span class="sxs-lookup"><span data-stu-id="8e296-124">Sets the NTP ending time value.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="8e296-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8e296-125">Requirements</span></span>



| <span data-ttu-id="8e296-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8e296-126">Requirement</span></span> | <span data-ttu-id="8e296-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8e296-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e296-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8e296-128">TAPI version</span></span><br/> | <span data-ttu-id="8e296-129">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8e296-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8e296-130">Header</span><span class="sxs-lookup"><span data-stu-id="8e296-130">Header</span></span><br/>       | <dl> <span data-ttu-id="8e296-131"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e296-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e296-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8e296-132">Library</span></span><br/>      | <dl> <span data-ttu-id="8e296-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e296-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8e296-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8e296-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="8e296-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e296-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

