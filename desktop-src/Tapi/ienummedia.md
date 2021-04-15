---
description: 'Интерфейс Иенуммедиа предоставляет стандартные методы перечисления COM для интерфейса Итмедиа. Метод Итмедиаколлектион:: Get \_ енумератиониф возвращает указатель на иенуммедиа.'
ms.assetid: 827f8866-2445-4b7c-88fe-eed19f48c93b
title: Интерфейс Иенуммедиа (Сдпблб. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7127e7d1d751ee487ad5b86326602cfcfe5aae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689433"
---
# <a name="ienummedia-interface"></a><span data-ttu-id="ebf6a-104">Интерфейс Иенуммедиа</span><span class="sxs-lookup"><span data-stu-id="ebf6a-104">IEnumMedia interface</span></span>

<span data-ttu-id="ebf6a-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ebf6a-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="ebf6a-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ebf6a-107">Интерфейс **иенуммедиа** предоставляет стандартные методы перечисления com для интерфейса [**итмедиа**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="ebf6a-107">The **IEnumMedia** interface provides COM-standard enumeration methods for the [**ITMedia**](itmedia.md) interface.</span></span> <span data-ttu-id="ebf6a-108">Метод [**итмедиаколлектион:: Get \_ енумератиониф**](itmediacollection-get-enumerationif.md) возвращает указатель на **иенуммедиа**.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-108">The [**ITMediaCollection::get\_EnumerationIf**](itmediacollection-get-enumerationif.md) method returns a pointer to **IEnumMedia**.</span></span>

## <a name="members"></a><span data-ttu-id="ebf6a-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="ebf6a-109">Members</span></span>

<span data-ttu-id="ebf6a-110">Интерфейс **иенуммедиа** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ebf6a-110">The **IEnumMedia** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ebf6a-111">**Иенуммедиа** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ebf6a-111">**IEnumMedia** also has these types of members:</span></span>

-   [<span data-ttu-id="ebf6a-112">Методы</span><span class="sxs-lookup"><span data-stu-id="ebf6a-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ebf6a-113">Методы</span><span class="sxs-lookup"><span data-stu-id="ebf6a-113">Methods</span></span>

<span data-ttu-id="ebf6a-114">Интерфейс **иенуммедиа** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-114">The **IEnumMedia** interface has these methods.</span></span>



| <span data-ttu-id="ebf6a-115">Метод</span><span class="sxs-lookup"><span data-stu-id="ebf6a-115">Method</span></span>                            | <span data-ttu-id="ebf6a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ebf6a-116">Description</span></span>                                                                                        |
|:----------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ebf6a-117">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="ebf6a-117">**Clone**</span></span>](ienummedia-clone.md) | <span data-ttu-id="ebf6a-118">Создает другой перечислитель с тем же состоянием перечисления, что и текущий.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="ebf6a-119">**Далее**</span><span class="sxs-lookup"><span data-stu-id="ebf6a-119">**Next**</span></span>](ienummedia-next.md)   | <span data-ttu-id="ebf6a-120">Возвращает указанное число следующих элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-120">Gets the next specified number of elements in the enumeration sequence.</span></span><br/>                 |
| [<span data-ttu-id="ebf6a-121">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="ebf6a-121">**Reset**</span></span>](ienummedia-reset.md) | <span data-ttu-id="ebf6a-122">Выполняет сброс до начала последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="ebf6a-123">**Пропустить**</span><span class="sxs-lookup"><span data-stu-id="ebf6a-123">**Skip**</span></span>](ienummedia-skip.md)   | <span data-ttu-id="ebf6a-124">Пропускает следующее заданное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="ebf6a-124">Skips over the next specified number of elements in the enumeration sequence.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="ebf6a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ebf6a-125">Requirements</span></span>



| <span data-ttu-id="ebf6a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ebf6a-126">Requirement</span></span> | <span data-ttu-id="ebf6a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ebf6a-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf6a-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="ebf6a-128">TAPI version</span></span><br/> | <span data-ttu-id="ebf6a-129">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ebf6a-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ebf6a-130">Header</span><span class="sxs-lookup"><span data-stu-id="ebf6a-130">Header</span></span><br/>       | <dl> <span data-ttu-id="ebf6a-131"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebf6a-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ebf6a-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ebf6a-132">Library</span></span><br/>      | <dl> <span data-ttu-id="ebf6a-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebf6a-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ebf6a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ebf6a-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="ebf6a-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebf6a-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

