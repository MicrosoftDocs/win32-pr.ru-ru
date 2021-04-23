---
description: 'Метод доступа к доступу извлекает диапазон времени, в течение которого поиск является эффективным. Этот метод реализует метод Имедиасикинг:: onavailable.'
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Метод Ксаурцесикинг. Available (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc661d81c49798b6fe06dc569b680e5f9839e5a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688935"
---
# <a name="csourceseekinggetavailable-method"></a><span data-ttu-id="63d6a-104">Ксаурцесикинг. доступный метод</span><span class="sxs-lookup"><span data-stu-id="63d6a-104">CSourceSeeking.GetAvailable method</span></span>

<span data-ttu-id="63d6a-105">`GetAvailable`Метод извлекает диапазон времени, в котором поиск является эффективным.</span><span class="sxs-lookup"><span data-stu-id="63d6a-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="63d6a-106">Этот метод реализует метод [**имедиасикинг:: onavailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .</span><span class="sxs-lookup"><span data-stu-id="63d6a-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="63d6a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63d6a-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="63d6a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="63d6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63d6a-109">*пеарлиест*</span><span class="sxs-lookup"><span data-stu-id="63d6a-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="63d6a-110">Указатель на переменную, которая получает самое раннее время для эффективного поиска.</span><span class="sxs-lookup"><span data-stu-id="63d6a-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span> <span data-ttu-id="63d6a-111">Переменная имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="63d6a-111">The variable is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="63d6a-112">*Пластина*</span><span class="sxs-lookup"><span data-stu-id="63d6a-112">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="63d6a-113">Указатель на переменную, которая получает Последнее время для эффективного поиска.</span><span class="sxs-lookup"><span data-stu-id="63d6a-113">Pointer to a variable that receives the latest time for efficient seeking.</span></span> <span data-ttu-id="63d6a-114">Переменной присваивается значение переменной-члена [**ксаурцесикинг:: m \_ ртдуратион**](csourceseeking-m-rtduration.md) .</span><span class="sxs-lookup"><span data-stu-id="63d6a-114">The variable is set to the value of the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63d6a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63d6a-115">Return value</span></span>

<span data-ttu-id="63d6a-116">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="63d6a-116">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="63d6a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="63d6a-117">Requirements</span></span>



| <span data-ttu-id="63d6a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="63d6a-118">Requirement</span></span> | <span data-ttu-id="63d6a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="63d6a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63d6a-120">Header</span><span class="sxs-lookup"><span data-stu-id="63d6a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="63d6a-121"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63d6a-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="63d6a-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="63d6a-122">Library</span></span><br/> | <dl> <span data-ttu-id="63d6a-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="63d6a-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63d6a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63d6a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63d6a-125">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="63d6a-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




