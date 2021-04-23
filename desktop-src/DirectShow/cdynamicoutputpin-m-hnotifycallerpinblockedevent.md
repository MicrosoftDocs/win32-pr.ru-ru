---
description: Событие, сообщающее о том, что ПИН-код успешно заблокирован, или пользователь отменяет незавершенный блок.
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: 'Элемент Кдинамикаутпутпин:: m_hNotifyCallerPinBlockedEvent (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hNotifyCallerPinBlockedEvent
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e28aa890e15602376b9500243a89e8f0e3d3bb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665247"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a><span data-ttu-id="9cb59-103">Элемент Кдинамикаутпутпин:: m \_ хнотификаллерпинблоккедевент</span><span class="sxs-lookup"><span data-stu-id="9cb59-103">CDynamicOutputPin::m\_hNotifyCallerPinBlockedEvent member</span></span>

<span data-ttu-id="9cb59-104">Событие, сообщающее о том, что ПИН-код успешно заблокирован, или пользователь отменяет незавершенный блок.</span><span class="sxs-lookup"><span data-stu-id="9cb59-104">Event that is signaled when the pin successfully blocks, or the user cancels a pending block.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cb59-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9cb59-105">Syntax</span></span>


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a><span data-ttu-id="9cb59-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="9cb59-106">Remarks</span></span>

<span data-ttu-id="9cb59-107">Прежде чем обращаться к этой переменной, удерживайте критический раздел [**кдинамикаутпутпин:: m \_ блоккстателокк**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="9cb59-107">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cb59-108">Требования</span><span class="sxs-lookup"><span data-stu-id="9cb59-108">Requirements</span></span>



| <span data-ttu-id="9cb59-109">Требование</span><span class="sxs-lookup"><span data-stu-id="9cb59-109">Requirement</span></span> | <span data-ttu-id="9cb59-110">Значение</span><span class="sxs-lookup"><span data-stu-id="9cb59-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cb59-111">Header</span><span class="sxs-lookup"><span data-stu-id="9cb59-111">Header</span></span><br/>  | <dl> <span data-ttu-id="9cb59-112"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9cb59-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9cb59-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9cb59-113">Library</span></span><br/> | <dl> <span data-ttu-id="9cb59-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9cb59-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cb59-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9cb59-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cb59-116">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="9cb59-116">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




