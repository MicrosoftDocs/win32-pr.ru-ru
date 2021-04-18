---
description: Хранит и извлекает сведения о подписках на события. Этот интерфейс расширяет интерфейс IEventSubscription2.
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: Интерфейс IEventSubscription3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: 94225faf957b2eac3388422d74df3cfdb8bf6d90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701279"
---
# <a name="ieventsubscription3-interface"></a><span data-ttu-id="27889-104">Интерфейс IEventSubscription3</span><span class="sxs-lookup"><span data-stu-id="27889-104">IEventSubscription3 interface</span></span>

<span data-ttu-id="27889-105">Хранит и извлекает сведения о подписках на события.</span><span class="sxs-lookup"><span data-stu-id="27889-105">Stores and retrieves information about event subscriptions.</span></span> <span data-ttu-id="27889-106">Этот интерфейс расширяет интерфейс [**IEventSubscription2**](ieventsubscription2.md) .</span><span class="sxs-lookup"><span data-stu-id="27889-106">This interface extends the [**IEventSubscription2**](ieventsubscription2.md) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="27889-107">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="27889-107">When to implement</span></span>

<span data-ttu-id="27889-108">Реализовывать интерфейс **IEventSubscription3** не требуется.</span><span class="sxs-lookup"><span data-stu-id="27889-108">You do not need to implement the **IEventSubscription3** interface.</span></span> <span data-ttu-id="27889-109">Предоставляемый системой класс объектов событий (CLSID \_ цевентсубскриптион) реализует **IEventSubscription3**.</span><span class="sxs-lookup"><span data-stu-id="27889-109">A system-supplied event object class (CLSID\_CEventSubscription) implements **IEventSubscription3**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="27889-110">Назначение</span><span class="sxs-lookup"><span data-stu-id="27889-110">When to use</span></span>

<span data-ttu-id="27889-111">Система [событий COM+](com--events.md) использует этот интерфейс для получения сведений об отдельных подписках.</span><span class="sxs-lookup"><span data-stu-id="27889-111">The [COM+ Events](com--events.md) system uses this interface to obtain information about individual subscriptions.</span></span>

## <a name="members"></a><span data-ttu-id="27889-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="27889-112">Members</span></span>

<span data-ttu-id="27889-113">Интерфейс **IEventSubscription3** наследует от **IEventSubscription2**.</span><span class="sxs-lookup"><span data-stu-id="27889-113">The **IEventSubscription3** interface inherits from **IEventSubscription2**.</span></span> <span data-ttu-id="27889-114">**IEventSubscription3** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="27889-114">**IEventSubscription3** also has these types of members:</span></span>

-   [<span data-ttu-id="27889-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="27889-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27889-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="27889-116">Properties</span></span>

<span data-ttu-id="27889-117">Интерфейс **IEventSubscription3** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="27889-117">The **IEventSubscription3** interface has these properties.</span></span>



| <span data-ttu-id="27889-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="27889-118">Property</span></span>                                                                                  | <span data-ttu-id="27889-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="27889-119">Access type</span></span>           | <span data-ttu-id="27889-120">Описание</span><span class="sxs-lookup"><span data-stu-id="27889-120">Description</span></span>                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="27889-121">**евентклассаппликатионид**</span><span class="sxs-lookup"><span data-stu-id="27889-121">**EventClassApplicationID**</span></span>](ieventsubscription3-eventclassapplicationid.md)<br/> | <span data-ttu-id="27889-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="27889-122">Read/write</span></span><br/> | <span data-ttu-id="27889-123">Идентификатор GUID приложения для объекта класса событий.</span><span class="sxs-lookup"><span data-stu-id="27889-123">The application GUID of the event class object.</span></span><br/> |
| [<span data-ttu-id="27889-124">**евенткласспартитионид**</span><span class="sxs-lookup"><span data-stu-id="27889-124">**EventClassPartitionID**</span></span>](ieventsubscription3-eventclasspartitionid.md)<br/>     | <span data-ttu-id="27889-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="27889-125">Read/write</span></span><br/> | <span data-ttu-id="27889-126">Идентификатор GUID раздела объекта класса событий.</span><span class="sxs-lookup"><span data-stu-id="27889-126">The partition GUID of the event class object.</span></span><br/>   |
| [<span data-ttu-id="27889-127">**субскрибераппликатионид**</span><span class="sxs-lookup"><span data-stu-id="27889-127">**SubscriberApplicationID**</span></span>](ieventsubscription3-subscriberapplicationid.md)<br/> | <span data-ttu-id="27889-128">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="27889-128">Read/write</span></span><br/> | <span data-ttu-id="27889-129">Идентификатор GUID приложения подписчика.</span><span class="sxs-lookup"><span data-stu-id="27889-129">The application GUID of the subscriber.</span></span><br/>         |
| [<span data-ttu-id="27889-130">**субскриберпартитионид**</span><span class="sxs-lookup"><span data-stu-id="27889-130">**SubscriberPartitionID**</span></span>](ieventsubscription3-subscriberpartitionid.md)<br/>     | <span data-ttu-id="27889-131">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="27889-131">Read/write</span></span><br/> | <span data-ttu-id="27889-132">Идентификатор GUID раздела подписчика.</span><span class="sxs-lookup"><span data-stu-id="27889-132">The partition GUID of the subscriber.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="27889-133">Требования</span><span class="sxs-lookup"><span data-stu-id="27889-133">Requirements</span></span>



| <span data-ttu-id="27889-134">Требование</span><span class="sxs-lookup"><span data-stu-id="27889-134">Requirement</span></span> | <span data-ttu-id="27889-135">Значение</span><span class="sxs-lookup"><span data-stu-id="27889-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="27889-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27889-136">Minimum supported client</span></span><br/> | <span data-ttu-id="27889-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="27889-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="27889-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27889-138">Minimum supported server</span></span><br/> | <span data-ttu-id="27889-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="27889-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="27889-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27889-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27889-141">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="27889-141">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




