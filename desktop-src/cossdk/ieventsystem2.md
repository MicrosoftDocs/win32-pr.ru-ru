---
description: Используется службой уведомлений о системных событиях Microsoft Internet Explorer (Сенс) для доступа к хранилищу данных событий. Этот интерфейс расширяет интерфейс Иевентсистем.
ms.assetid: ad3c38a6-fa2d-4fcd-8782-1fac7595e829
title: Интерфейс IEventSystem2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a174c9457dc347257677e8111772ad14f0dc9fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496452"
---
# <a name="ieventsystem2-interface"></a><span data-ttu-id="a4e5e-104">Интерфейс IEventSystem2</span><span class="sxs-lookup"><span data-stu-id="a4e5e-104">IEventSystem2 interface</span></span>

<span data-ttu-id="a4e5e-105">Используется службой уведомлений о системных событиях Microsoft Internet Explorer (Сенс) для доступа к хранилищу данных событий.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-105">Used by the Microsoft Internet Explorer System Event Notification Service (SENS) to access the event data store.</span></span> <span data-ttu-id="a4e5e-106">Этот интерфейс расширяет интерфейс [**иевентсистем**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) .</span><span class="sxs-lookup"><span data-stu-id="a4e5e-106">This interface extends the [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="a4e5e-107">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="a4e5e-107">When to implement</span></span>

<span data-ttu-id="a4e5e-108">Реализовывать интерфейс **IEventSystem2** не требуется.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-108">You do not need to implement the **IEventSystem2** interface.</span></span> <span data-ttu-id="a4e5e-109">Предоставляемый системой системный объект событий (CLSID \_ цевентсистем) реализует **IEventSystem2**.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-109">A system-supplied event system object (CLSID\_CEventSystem) implements **IEventSystem2**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="a4e5e-110">Назначение</span><span class="sxs-lookup"><span data-stu-id="a4e5e-110">When to use</span></span>

<span data-ttu-id="a4e5e-111">При использовании Сенс можно вызывать методы **IEventSystem2** для добавления и удаления объектов из хранилища событий и получения объектов из хранилища событий.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-111">If you use SENS, you can call the methods of **IEventSystem2** to add and remove objects to and from the event store and to obtain objects from the event store.</span></span>

<span data-ttu-id="a4e5e-112">Поскольку [**иевентпублишер**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) и объект издателя больше не поддерживаются, [**иевентобжектчанже**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) не вызывается в методе [**чанжедпублишер**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) .</span><span class="sxs-lookup"><span data-stu-id="a4e5e-112">Because [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) and the publisher object are no longer supported, [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) is not called on the [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) method.</span></span>

## <a name="members"></a><span data-ttu-id="a4e5e-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="a4e5e-113">Members</span></span>

<span data-ttu-id="a4e5e-114">Интерфейс **IEventSystem2** наследует от **иевентсистем**.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-114">The **IEventSystem2** interface inherits from **IEventSystem**.</span></span> <span data-ttu-id="a4e5e-115">**IEventSystem2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a4e5e-115">**IEventSystem2** also has these types of members:</span></span>

-   [<span data-ttu-id="a4e5e-116">Методы</span><span class="sxs-lookup"><span data-stu-id="a4e5e-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a4e5e-117">Методы</span><span class="sxs-lookup"><span data-stu-id="a4e5e-117">Methods</span></span>

<span data-ttu-id="a4e5e-118">Интерфейс **IEventSystem2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-118">The **IEventSystem2** interface has these methods.</span></span>



| <span data-ttu-id="a4e5e-119">Метод</span><span class="sxs-lookup"><span data-stu-id="a4e5e-119">Method</span></span>                                                                         | <span data-ttu-id="a4e5e-120">Описание</span><span class="sxs-lookup"><span data-stu-id="a4e5e-120">Description</span></span>                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="a4e5e-121">**GetVersion**</span><span class="sxs-lookup"><span data-stu-id="a4e5e-121">**GetVersion**</span></span>](ieventsystem2-getversion.md)                                 | <span data-ttu-id="a4e5e-122">Возвращает номер версии системы событий.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-122">Retrieves the version number of the event system.</span></span><br/>                      |
| [<span data-ttu-id="a4e5e-123">**верифитрансиентсубскриберс**</span><span class="sxs-lookup"><span data-stu-id="a4e5e-123">**VerifyTransientSubscribers**</span></span>](ieventsystem2-verifytransientsubscribers.md) | <span data-ttu-id="a4e5e-124">Проверяет существование всех временных подписчиков в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-124">Verifies the existence of all transient subscribers in the data store.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a4e5e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a4e5e-125">Requirements</span></span>



| <span data-ttu-id="a4e5e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="a4e5e-126">Requirement</span></span> | <span data-ttu-id="a4e5e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a4e5e-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a4e5e-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4e5e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a4e5e-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a4e5e-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a4e5e-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4e5e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a4e5e-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a4e5e-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a4e5e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4e5e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4e5e-133">**иевентсистем**</span><span class="sxs-lookup"><span data-stu-id="a4e5e-133">**IEventSystem**</span></span>](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

