---
description: 'Идентификатор потока, который последним вызвал метод Ипинфловконтрол:: Block для этого ПИН-кода. Эта переменная-член допустима только в том случае, если ПИН-код заблокирован.'
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: 'Элемент Кдинамикаутпутпин:: m_dwBlockCallerThreadID (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9aa2de66f1afe690715ab658483c01cdfeb3f451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658076"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a><span data-ttu-id="9ad12-104">Элемент Кдинамикаутпутпин:: m \_ двблокккаллерсреадид</span><span class="sxs-lookup"><span data-stu-id="9ad12-104">CDynamicOutputPin::m\_dwBlockCallerThreadID member</span></span>

<span data-ttu-id="9ad12-105">Идентификатор потока, который последним вызвал метод [**ипинфловконтрол:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) для этого ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="9ad12-105">The identifier of the thread that last called the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) method on this pin.</span></span> <span data-ttu-id="9ad12-106">Эта переменная-член допустима только в том случае, если ПИН-код заблокирован.</span><span class="sxs-lookup"><span data-stu-id="9ad12-106">This member variable is only valid while the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ad12-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ad12-107">Syntax</span></span>


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a><span data-ttu-id="9ad12-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="9ad12-108">Remarks</span></span>

<span data-ttu-id="9ad12-109">Прежде чем обращаться к этой переменной, удерживайте критический раздел [**кдинамикаутпутпин:: m \_ блоккстателокк**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="9ad12-109">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ad12-110">Требования</span><span class="sxs-lookup"><span data-stu-id="9ad12-110">Requirements</span></span>



| <span data-ttu-id="9ad12-111">Требование</span><span class="sxs-lookup"><span data-stu-id="9ad12-111">Requirement</span></span> | <span data-ttu-id="9ad12-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9ad12-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad12-113">Header</span><span class="sxs-lookup"><span data-stu-id="9ad12-113">Header</span></span><br/>  | <dl> <span data-ttu-id="9ad12-114"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ad12-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9ad12-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9ad12-115">Library</span></span><br/> | <dl> <span data-ttu-id="9ad12-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9ad12-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ad12-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ad12-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ad12-118">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="9ad12-118">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




