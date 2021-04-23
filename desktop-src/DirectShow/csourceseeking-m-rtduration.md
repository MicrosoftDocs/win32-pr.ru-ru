---
description: 'Длительность потока. По умолчанию в качестве значения задается значение переменной-члена Ксаурцесикинг:: m \_ ртстоп.'
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: 'Элемент Ксаурцесикинг:: m_rtDuration (Ктлутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e188a29689a6dd1a54ef401f8bd2677e30989972
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657495"
---
# <a name="csourceseekingm_rtduration-member"></a><span data-ttu-id="02f07-104">Элемент Ксаурцесикинг:: m \_ ртдуратион</span><span class="sxs-lookup"><span data-stu-id="02f07-104">CSourceSeeking::m\_rtDuration member</span></span>

<span data-ttu-id="02f07-105">Длительность потока.</span><span class="sxs-lookup"><span data-stu-id="02f07-105">Duration of the stream.</span></span> <span data-ttu-id="02f07-106">По умолчанию в качестве значения задается значение переменной-члена [**ксаурцесикинг:: m \_ ртстоп**](csourceseeking-m-rtstop.md) .</span><span class="sxs-lookup"><span data-stu-id="02f07-106">By default, the value is set to the value of the [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f07-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02f07-107">Syntax</span></span>


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a><span data-ttu-id="02f07-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="02f07-108">Remarks</span></span>

<span data-ttu-id="02f07-109">Чтобы получить доступ к этой переменной, удерживайте критический раздел **m \_ плокк** .</span><span class="sxs-lookup"><span data-stu-id="02f07-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f07-110">Требования</span><span class="sxs-lookup"><span data-stu-id="02f07-110">Requirements</span></span>



| <span data-ttu-id="02f07-111">Требование</span><span class="sxs-lookup"><span data-stu-id="02f07-111">Requirement</span></span> | <span data-ttu-id="02f07-112">Значение</span><span class="sxs-lookup"><span data-stu-id="02f07-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02f07-113">Header</span><span class="sxs-lookup"><span data-stu-id="02f07-113">Header</span></span><br/>  | <dl> <span data-ttu-id="02f07-114"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02f07-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="02f07-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="02f07-115">Library</span></span><br/> | <dl> <span data-ttu-id="02f07-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="02f07-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02f07-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02f07-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f07-118">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="02f07-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




