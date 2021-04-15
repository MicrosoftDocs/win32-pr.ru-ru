---
description: 'Интерфейс Иенумтиме предоставляет стандартные методы перечисления COM для интерфейса Иттиме. Метод Иттимеколлектион:: Get \_ енумератиониф возвращает указатель на иенумтиме.'
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: Интерфейс Иенумтиме (Сдпблб. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2336f435ec322694847c776ac92ade93e8791207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675635"
---
# <a name="ienumtime-interface"></a><span data-ttu-id="6c9bf-104">Интерфейс Иенумтиме</span><span class="sxs-lookup"><span data-stu-id="6c9bf-104">IEnumTime interface</span></span>

<span data-ttu-id="6c9bf-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6c9bf-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="6c9bf-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6c9bf-107">Интерфейс **иенумтиме** предоставляет стандартные методы перечисления com для интерфейса [**иттиме**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="6c9bf-107">The **IEnumTime** interface provides COM-standard enumeration methods for the [**ITTime**](ittime.md) interface.</span></span> <span data-ttu-id="6c9bf-108">Метод [**иттимеколлектион:: Get \_ енумератиониф**](ittimecollection-get-enumerationif.md) возвращает указатель на **иенумтиме**.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-108">The [**ITTimeCollection::get\_EnumerationIf**](ittimecollection-get-enumerationif.md) method returns a pointer to **IEnumTime**.</span></span>

## <a name="members"></a><span data-ttu-id="6c9bf-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="6c9bf-109">Members</span></span>

<span data-ttu-id="6c9bf-110">Интерфейс **иенумтиме** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6c9bf-110">The **IEnumTime** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6c9bf-111">**Иенумтиме** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6c9bf-111">**IEnumTime** also has these types of members:</span></span>

-   [<span data-ttu-id="6c9bf-112">Методы</span><span class="sxs-lookup"><span data-stu-id="6c9bf-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6c9bf-113">Методы</span><span class="sxs-lookup"><span data-stu-id="6c9bf-113">Methods</span></span>

<span data-ttu-id="6c9bf-114">Интерфейс **иенумтиме** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-114">The **IEnumTime** interface has these methods.</span></span>



| <span data-ttu-id="6c9bf-115">Метод</span><span class="sxs-lookup"><span data-stu-id="6c9bf-115">Method</span></span>                           | <span data-ttu-id="6c9bf-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6c9bf-116">Description</span></span>                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c9bf-117">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="6c9bf-117">**Clone**</span></span>](ienumtime-clone.md) | <span data-ttu-id="6c9bf-118">Создает другой перечислитель с тем же состоянием перечисления, что и текущий.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="6c9bf-119">**Далее**</span><span class="sxs-lookup"><span data-stu-id="6c9bf-119">**Next**</span></span>](ienumtime-next.md)   | <span data-ttu-id="6c9bf-120">Возвращает указанное число следующих элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-120">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="6c9bf-121">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="6c9bf-121">**Reset**</span></span>](ienumtime-reset.md) | <span data-ttu-id="6c9bf-122">Выполняет сброс до начала последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="6c9bf-123">**Пропустить**</span><span class="sxs-lookup"><span data-stu-id="6c9bf-123">**Skip**</span></span>](ienumtime-skip.md)   | <span data-ttu-id="6c9bf-124">Пропускает следующее заданное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-124">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="6c9bf-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6c9bf-125">Requirements</span></span>



| <span data-ttu-id="6c9bf-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6c9bf-126">Requirement</span></span> | <span data-ttu-id="6c9bf-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6c9bf-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c9bf-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="6c9bf-128">TAPI version</span></span><br/> | <span data-ttu-id="6c9bf-129">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6c9bf-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6c9bf-130">Header</span><span class="sxs-lookup"><span data-stu-id="6c9bf-130">Header</span></span><br/>       | <dl> <span data-ttu-id="6c9bf-131"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c9bf-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c9bf-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6c9bf-132">Library</span></span><br/>      | <dl> <span data-ttu-id="6c9bf-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c9bf-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6c9bf-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6c9bf-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="6c9bf-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c9bf-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

