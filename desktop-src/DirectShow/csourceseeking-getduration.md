---
description: Ксаурцесикинг. Duration-метод — метод методаической длительности извлекает длительность потока. Этот метод реализует метод Имедиасикинг::/Duration.
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Ксаурцесикинг. метод Duration (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d5b961ad62d65c1f728af71e82de1373ea20b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098772"
---
# <a name="csourceseekinggetduration-method"></a><span data-ttu-id="7f3bc-104">Ксаурцесикинг. метод Duration</span><span class="sxs-lookup"><span data-stu-id="7f3bc-104">CSourceSeeking.GetDuration method</span></span>

<span data-ttu-id="7f3bc-105">`GetDuration`Метод получает длительность потока.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="7f3bc-106">Этот метод реализует метод [**имедиасикинг::/Duration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .</span><span class="sxs-lookup"><span data-stu-id="7f3bc-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f3bc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f3bc-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="7f3bc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f3bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f3bc-109">*пдуратион*</span><span class="sxs-lookup"><span data-stu-id="7f3bc-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="7f3bc-110">Указатель на переменную, которая получает длительность в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f3bc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f3bc-111">Return value</span></span>

<span data-ttu-id="7f3bc-112">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7f3bc-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="7f3bc-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7f3bc-113">Return code</span></span>                                                                               | <span data-ttu-id="7f3bc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="7f3bc-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="7f3bc-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7f3bc-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="7f3bc-116">Успешное завершение</span><span class="sxs-lookup"><span data-stu-id="7f3bc-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="7f3bc-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="7f3bc-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="7f3bc-118">Значение указателя **null**</span><span class="sxs-lookup"><span data-stu-id="7f3bc-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7f3bc-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="7f3bc-119">Remarks</span></span>

<span data-ttu-id="7f3bc-120">Длительность задается переменной-членом [**ксаурцесикинг:: m \_ ртдуратион**](csourceseeking-m-rtduration.md) .</span><span class="sxs-lookup"><span data-stu-id="7f3bc-120">The duration is specified by the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f3bc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7f3bc-121">Requirements</span></span>



| <span data-ttu-id="7f3bc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7f3bc-122">Requirement</span></span> | <span data-ttu-id="7f3bc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7f3bc-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f3bc-124">Header</span><span class="sxs-lookup"><span data-stu-id="7f3bc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7f3bc-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f3bc-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f3bc-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7f3bc-126">Library</span></span><br/> | <dl> <span data-ttu-id="7f3bc-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7f3bc-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f3bc-128">См. также</span><span class="sxs-lookup"><span data-stu-id="7f3bc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f3bc-129">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="7f3bc-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




