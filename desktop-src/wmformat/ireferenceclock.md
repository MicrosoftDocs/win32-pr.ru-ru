---
title: Интерфейс Иреференцеклокк
description: Интерфейс Иреференцеклокк предоставляет доступ к внешним часам. Этот интерфейс обеспечивает синхронизацию всех подпрограмм подготовки к одному и тому же часам. Этот интерфейс можно получить из объекта модуля чтения.
ms.assetid: 1424fd74-d56c-4338-801f-319ef975169f
keywords:
- Формат Windows Media в интерфейсе Иреференцеклокк
- Иреференцеклокк интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IReferenceClock
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72d17ef362aa5436fe98443d86dff5ae31212650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700871"
---
# <a name="ireferenceclock-interface"></a><span data-ttu-id="86db5-106">Интерфейс Иреференцеклокк</span><span class="sxs-lookup"><span data-stu-id="86db5-106">IReferenceClock interface</span></span>

<span data-ttu-id="86db5-107">Интерфейс **иреференцеклокк** предоставляет доступ к внешним часам.</span><span class="sxs-lookup"><span data-stu-id="86db5-107">The **IReferenceClock** interface provides access to an external clock.</span></span> <span data-ttu-id="86db5-108">Этот интерфейс обеспечивает синхронизацию всех подпрограмм подготовки к одному и тому же часам.</span><span class="sxs-lookup"><span data-stu-id="86db5-108">This interface is provided to enable all rendering routines to be synchronized to the same clock.</span></span>

<span data-ttu-id="86db5-109">Этот интерфейс можно получить из объекта модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="86db5-109">This interface can be obtained from a reader object.</span></span>

## <a name="members"></a><span data-ttu-id="86db5-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="86db5-110">Members</span></span>

<span data-ttu-id="86db5-111">Интерфейс **иреференцеклокк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="86db5-111">The **IReferenceClock** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="86db5-112">**Иреференцеклокк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="86db5-112">**IReferenceClock** also has these types of members:</span></span>

-   [<span data-ttu-id="86db5-113">Методы</span><span class="sxs-lookup"><span data-stu-id="86db5-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="86db5-114">Методы</span><span class="sxs-lookup"><span data-stu-id="86db5-114">Methods</span></span>

<span data-ttu-id="86db5-115">Интерфейс **иреференцеклокк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="86db5-115">The **IReferenceClock** interface has these methods.</span></span>



| <span data-ttu-id="86db5-116">Метод</span><span class="sxs-lookup"><span data-stu-id="86db5-116">Method</span></span>                                                   | <span data-ttu-id="86db5-117">Описание</span><span class="sxs-lookup"><span data-stu-id="86db5-117">Description</span></span>                                                               |
|:---------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="86db5-118">**адвисепериодик**</span><span class="sxs-lookup"><span data-stu-id="86db5-118">**AdvisePeriodic**</span></span>](ireferenceclock-adviseperiodic.md) | <span data-ttu-id="86db5-119">Не реализовано в этом пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="86db5-119">Not implemented by this SDK.</span></span><br/>                                   |
| [<span data-ttu-id="86db5-120">**адвисетиме**</span><span class="sxs-lookup"><span data-stu-id="86db5-120">**AdviseTime**</span></span>](ireferenceclock-advisetime.md)         | <span data-ttu-id="86db5-121">Запрашивает асинхронное уведомление об истечении времени.</span><span class="sxs-lookup"><span data-stu-id="86db5-121">Requests an asynchronous notification that a time has elapsed.</span></span><br/> |
| [<span data-ttu-id="86db5-122">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="86db5-122">**GetTime**</span></span>](ireferenceclock-gettime.md)               | <span data-ttu-id="86db5-123">Извлекает текущее время ссылки.</span><span class="sxs-lookup"><span data-stu-id="86db5-123">Retrieves the current reference time.</span></span><br/>                          |
| [<span data-ttu-id="86db5-124">**Unadvise**</span><span class="sxs-lookup"><span data-stu-id="86db5-124">**Unadvise**</span></span>](ireferenceclock-unadvise.md)             | <span data-ttu-id="86db5-125">Отменяет запрос на уведомление.</span><span class="sxs-lookup"><span data-stu-id="86db5-125">Cancels a notification request.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="86db5-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86db5-126">Remarks</span></span>

<span data-ttu-id="86db5-127">Сведения о других интерфейсах, которые можно получить с помощью метода QueryInterface этого интерфейса, см. в разделе объект Reader.</span><span class="sxs-lookup"><span data-stu-id="86db5-127">For information on other interfaces that can be obtained by using the QueryInterface method of this interface, see Reader Object.</span></span>

## <a name="see-also"></a><span data-ttu-id="86db5-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86db5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86db5-129">**Интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="86db5-129">**Interfaces**</span></span>](interfaces.md)
</dt> </dl>

 

