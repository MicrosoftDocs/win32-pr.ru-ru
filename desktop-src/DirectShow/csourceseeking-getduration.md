---
description: Метод методаической длительности извлекает длительность потока. Этот метод реализует метод Имедиасикинг::/Duration.
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
ms.openlocfilehash: 8368f655394089c1155d848bc53d2ba2375e3320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657507"
---
# <a name="csourceseekinggetduration-method"></a><span data-ttu-id="abb7b-104">Ксаурцесикинг. метод Duration</span><span class="sxs-lookup"><span data-stu-id="abb7b-104">CSourceSeeking.GetDuration method</span></span>

<span data-ttu-id="abb7b-105">`GetDuration`Метод получает длительность потока.</span><span class="sxs-lookup"><span data-stu-id="abb7b-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="abb7b-106">Этот метод реализует метод [**имедиасикинг::/Duration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .</span><span class="sxs-lookup"><span data-stu-id="abb7b-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="abb7b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abb7b-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="abb7b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="abb7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abb7b-109">*пдуратион*</span><span class="sxs-lookup"><span data-stu-id="abb7b-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="abb7b-110">Указатель на переменную, которая получает длительность в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="abb7b-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abb7b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abb7b-111">Return value</span></span>

<span data-ttu-id="abb7b-112">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="abb7b-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="abb7b-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="abb7b-113">Return code</span></span>                                                                               | <span data-ttu-id="abb7b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="abb7b-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="abb7b-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="abb7b-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="abb7b-116">Успешно</span><span class="sxs-lookup"><span data-stu-id="abb7b-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="abb7b-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="abb7b-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="abb7b-118">Значение указателя **null**</span><span class="sxs-lookup"><span data-stu-id="abb7b-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="abb7b-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abb7b-119">Remarks</span></span>

<span data-ttu-id="abb7b-120">Длительность задается переменной-членом [**ксаурцесикинг:: m \_ ртдуратион**](csourceseeking-m-rtduration.md) .</span><span class="sxs-lookup"><span data-stu-id="abb7b-120">The duration is specified by the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="abb7b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="abb7b-121">Requirements</span></span>



| <span data-ttu-id="abb7b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="abb7b-122">Requirement</span></span> | <span data-ttu-id="abb7b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="abb7b-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abb7b-124">Header</span><span class="sxs-lookup"><span data-stu-id="abb7b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="abb7b-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="abb7b-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="abb7b-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="abb7b-126">Library</span></span><br/> | <dl> <span data-ttu-id="abb7b-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="abb7b-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abb7b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abb7b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abb7b-129">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="abb7b-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




