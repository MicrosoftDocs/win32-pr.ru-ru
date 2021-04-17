---
description: Хранит и извлекает сведения о подписках на события. Этот интерфейс расширяет интерфейс Иевентсубскриптион.
ms.assetid: f153afb7-c897-40f8-81ed-50308844cac5
title: Интерфейс IEventSubscription2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc7e3e41efc4b44c00c23f0910b8b696940fc1df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682366"
---
# <a name="ieventsubscription2-interface"></a><span data-ttu-id="74454-104">Интерфейс IEventSubscription2</span><span class="sxs-lookup"><span data-stu-id="74454-104">IEventSubscription2 interface</span></span>

<span data-ttu-id="74454-105">Хранит и извлекает сведения о подписках на события.</span><span class="sxs-lookup"><span data-stu-id="74454-105">Stores and retrieves information about event subscriptions.</span></span> <span data-ttu-id="74454-106">Этот интерфейс расширяет интерфейс [**иевентсубскриптион**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) .</span><span class="sxs-lookup"><span data-stu-id="74454-106">This interface extends the [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="74454-107">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="74454-107">When to implement</span></span>

<span data-ttu-id="74454-108">Реализовывать интерфейс **IEventSubscription2** не требуется.</span><span class="sxs-lookup"><span data-stu-id="74454-108">You do not need to implement the **IEventSubscription2** interface.</span></span> <span data-ttu-id="74454-109">Предоставляемый системой класс объектов событий (CLSID \_ цевентсубскриптион) реализует **IEventSubscription2**.</span><span class="sxs-lookup"><span data-stu-id="74454-109">A system-supplied event object class (CLSID\_CEventSubscription) implements **IEventSubscription2**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="74454-110">Назначение</span><span class="sxs-lookup"><span data-stu-id="74454-110">When to use</span></span>

<span data-ttu-id="74454-111">Система [событий COM+](com--events.md) использует этот интерфейс для получения сведений об отдельных подписках.</span><span class="sxs-lookup"><span data-stu-id="74454-111">The [COM+ Events](com--events.md) system uses this interface to obtain information about individual subscriptions.</span></span>

## <a name="members"></a><span data-ttu-id="74454-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="74454-112">Members</span></span>

<span data-ttu-id="74454-113">Интерфейс **IEventSubscription2** наследует от **иевентсубскриптион**.</span><span class="sxs-lookup"><span data-stu-id="74454-113">The **IEventSubscription2** interface inherits from **IEventSubscription**.</span></span> <span data-ttu-id="74454-114">**IEventSubscription2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="74454-114">**IEventSubscription2** also has these types of members:</span></span>

-   [<span data-ttu-id="74454-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="74454-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74454-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="74454-116">Properties</span></span>

<span data-ttu-id="74454-117">Интерфейс **IEventSubscription2** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="74454-117">The **IEventSubscription2** interface has these properties.</span></span>



| <span data-ttu-id="74454-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="74454-118">Property</span></span>                                                                      | <span data-ttu-id="74454-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="74454-119">Access type</span></span>           | <span data-ttu-id="74454-120">Описание</span><span class="sxs-lookup"><span data-stu-id="74454-120">Description</span></span>                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="74454-121">**Параметром filterCriteria**</span><span class="sxs-lookup"><span data-stu-id="74454-121">**FilterCriteria**</span></span>](ieventsubscription2-filtercriteria.md)<br/>       | <span data-ttu-id="74454-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="74454-122">Read/write</span></span><br/> | <span data-ttu-id="74454-123">Критерии фильтра, управляющие подпиской.</span><span class="sxs-lookup"><span data-stu-id="74454-123">The filter criteria governing the subscription.</span></span><br/> |
| [<span data-ttu-id="74454-124">**субскрибермоникер**</span><span class="sxs-lookup"><span data-stu-id="74454-124">**SubscriberMoniker**</span></span>](ieventsubscription2-subscribermoniker.md)<br/> | <span data-ttu-id="74454-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="74454-125">Read/write</span></span><br/> | <span data-ttu-id="74454-126">Моникер подписчика.</span><span class="sxs-lookup"><span data-stu-id="74454-126">The subscriber's moniker.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="74454-127">Требования</span><span class="sxs-lookup"><span data-stu-id="74454-127">Requirements</span></span>



| <span data-ttu-id="74454-128">Требование</span><span class="sxs-lookup"><span data-stu-id="74454-128">Requirement</span></span> | <span data-ttu-id="74454-129">Значение</span><span class="sxs-lookup"><span data-stu-id="74454-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="74454-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74454-130">Minimum supported client</span></span><br/> | <span data-ttu-id="74454-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="74454-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="74454-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74454-132">Minimum supported server</span></span><br/> | <span data-ttu-id="74454-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="74454-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="74454-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74454-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74454-135">**иевентсубскриптион**</span><span class="sxs-lookup"><span data-stu-id="74454-135">**IEventSubscription**</span></span>](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




