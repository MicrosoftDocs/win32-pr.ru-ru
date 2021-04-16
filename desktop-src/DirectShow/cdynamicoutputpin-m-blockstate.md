---
description: Состояние блокировки.
ms.assetid: 55afd314-efd3-47bf-80e3-e17c1332a4cf
title: 'Элемент Кдинамикаутпутпин:: m_BlockState (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockState
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f02a59854b381db5e7b13a85ccca0754cc38f51d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658043"
---
# <a name="cdynamicoutputpinm_blockstate-member"></a><span data-ttu-id="1000a-103">Элемент Кдинамикаутпутпин:: m \_ блоккстате</span><span class="sxs-lookup"><span data-stu-id="1000a-103">CDynamicOutputPin::m\_BlockState member</span></span>

<span data-ttu-id="1000a-104">Состояние блокировки.</span><span class="sxs-lookup"><span data-stu-id="1000a-104">Blocking state.</span></span>

## <a name="syntax"></a><span data-ttu-id="1000a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1000a-105">Syntax</span></span>


```C++
BLOCK_STATE m_BlockState;
```



## <a name="remarks"></a><span data-ttu-id="1000a-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="1000a-106">Remarks</span></span>

<span data-ttu-id="1000a-107">Определены следующие состояния:</span><span class="sxs-lookup"><span data-stu-id="1000a-107">The following states are defined:</span></span>

-   <span data-ttu-id="1000a-108">НЕ \_ заблокировано</span><span class="sxs-lookup"><span data-stu-id="1000a-108">NOT\_BLOCKED</span></span>
-   <span data-ttu-id="1000a-109">PENDING</span><span class="sxs-lookup"><span data-stu-id="1000a-109">PENDING</span></span>
-   <span data-ttu-id="1000a-110">БЛОКИРУЕТ</span><span class="sxs-lookup"><span data-stu-id="1000a-110">BLOCKED</span></span>

<span data-ttu-id="1000a-111">Прежде чем обращаться к этой переменной, удерживайте критический раздел [**кдинамикаутпутпин:: m \_ блоккстателокк**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="1000a-111">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="1000a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="1000a-112">Requirements</span></span>



| <span data-ttu-id="1000a-113">Требование</span><span class="sxs-lookup"><span data-stu-id="1000a-113">Requirement</span></span> | <span data-ttu-id="1000a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1000a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1000a-115">Header</span><span class="sxs-lookup"><span data-stu-id="1000a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="1000a-116"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1000a-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1000a-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1000a-117">Library</span></span><br/> | <dl> <span data-ttu-id="1000a-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1000a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1000a-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1000a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1000a-120">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="1000a-120">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




