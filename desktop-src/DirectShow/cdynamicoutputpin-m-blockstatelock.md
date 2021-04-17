---
description: Критическая секция, защищающая состояние блокировки.
ms.assetid: 6d20cf4c-2c27-41e6-8d01-6cb5e3876a38
title: 'Элемент Кдинамикаутпутпин:: m_BlockStateLock (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d9175342218e8b82698fe9b89d15937d6913e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657286"
---
# <a name="cdynamicoutputpinm_blockstatelock-member"></a><span data-ttu-id="7ae8f-103">Элемент Кдинамикаутпутпин:: m \_ блоккстателокк</span><span class="sxs-lookup"><span data-stu-id="7ae8f-103">CDynamicOutputPin::m\_BlockStateLock member</span></span>

<span data-ttu-id="7ae8f-104">Критическая секция, защищающая состояние блокировки.</span><span class="sxs-lookup"><span data-stu-id="7ae8f-104">Critical section that protects the blocking state.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae8f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ae8f-105">Syntax</span></span>


```C++
CCritSec m_BlockStateLock;
```



## <a name="remarks"></a><span data-ttu-id="7ae8f-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ae8f-106">Remarks</span></span>

<span data-ttu-id="7ae8f-107">Перед использованием любой из следующих переменных члена следует сохранить этот критический раздел:</span><span class="sxs-lookup"><span data-stu-id="7ae8f-107">Hold this critical section before using any of the following member variables:</span></span>

-   [<span data-ttu-id="7ae8f-108">**Кдинамикаутпутпин:: m \_ блоккстате**</span><span class="sxs-lookup"><span data-stu-id="7ae8f-108">**CDynamicOutputPin::m\_BlockState**</span></span>](cdynamicoutputpin-m-blockstate.md)
-   [<span data-ttu-id="7ae8f-109">**Кдинамикаутпутпин:: m \_ двблокккаллерсреадид**</span><span class="sxs-lookup"><span data-stu-id="7ae8f-109">**CDynamicOutputPin::m\_dwBlockCallerThreadID**</span></span>](cdynamicoutputpin-m-dwblockcallerthreadid.md)
-   [<span data-ttu-id="7ae8f-110">**Кдинамикаутпутпин:: m \_ двнумаутстандингаутпутпинусерс**</span><span class="sxs-lookup"><span data-stu-id="7ae8f-110">**CDynamicOutputPin::m\_dwNumOutstandingOutputPinUsers**</span></span>](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md)
-   [<span data-ttu-id="7ae8f-111">**Кдинамикаутпутпин:: m \_ хнотификаллерпинблоккедевент**</span><span class="sxs-lookup"><span data-stu-id="7ae8f-111">**CDynamicOutputPin::m\_hNotifyCallerPinBlockedEvent**</span></span>](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)

## <a name="requirements"></a><span data-ttu-id="7ae8f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7ae8f-112">Requirements</span></span>



| <span data-ttu-id="7ae8f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7ae8f-113">Requirement</span></span> | <span data-ttu-id="7ae8f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7ae8f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae8f-115">Header</span><span class="sxs-lookup"><span data-stu-id="7ae8f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="7ae8f-116"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ae8f-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7ae8f-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7ae8f-117">Library</span></span><br/> | <dl> <span data-ttu-id="7ae8f-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7ae8f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ae8f-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ae8f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ae8f-120">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="7ae8f-120">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




