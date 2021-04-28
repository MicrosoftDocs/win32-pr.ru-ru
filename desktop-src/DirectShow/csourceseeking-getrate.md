---
description: 'Ксаурцесикинг. метод Rate — метод метода Rate извлекает скорость воспроизведения. Этот метод реализует метод Имедиасикинг:: Rate.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Метод Ксаурцесикинг. rate (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fef379ef06cd0982f1eb5742ac2624d706ed73a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085232"
---
# <a name="csourceseekinggetrate-method"></a><span data-ttu-id="b6cfc-104">Ксаурцесикинг. метод Rate</span><span class="sxs-lookup"><span data-stu-id="b6cfc-104">CSourceSeeking.GetRate method</span></span>

<span data-ttu-id="b6cfc-105">`GetRate`Метод получает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b6cfc-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="b6cfc-106">Этот метод реализует метод [**имедиасикинг:: Rate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .</span><span class="sxs-lookup"><span data-stu-id="b6cfc-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6cfc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6cfc-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="b6cfc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6cfc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6cfc-109">*пдрате*</span><span class="sxs-lookup"><span data-stu-id="b6cfc-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="b6cfc-110">Указатель на переменную, которая получает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b6cfc-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6cfc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6cfc-111">Return value</span></span>

<span data-ttu-id="b6cfc-112">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b6cfc-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="b6cfc-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b6cfc-113">Return code</span></span>                                                                               | <span data-ttu-id="b6cfc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b6cfc-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="b6cfc-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b6cfc-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b6cfc-116">Успешное завершение</span><span class="sxs-lookup"><span data-stu-id="b6cfc-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="b6cfc-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="b6cfc-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b6cfc-118">Значение указателя **null**</span><span class="sxs-lookup"><span data-stu-id="b6cfc-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b6cfc-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="b6cfc-119">Remarks</span></span>

<span data-ttu-id="b6cfc-120">Скорость воспроизведения задается переменной-членом [**ксаурцесикинг:: m \_ дратесикинг**](csourceseeking-m-drateseeking.md) .</span><span class="sxs-lookup"><span data-stu-id="b6cfc-120">The playback rate is specified by the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6cfc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b6cfc-121">Requirements</span></span>



| <span data-ttu-id="b6cfc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b6cfc-122">Requirement</span></span> | <span data-ttu-id="b6cfc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b6cfc-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6cfc-124">Header</span><span class="sxs-lookup"><span data-stu-id="b6cfc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b6cfc-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6cfc-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b6cfc-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b6cfc-126">Library</span></span><br/> | <dl> <span data-ttu-id="b6cfc-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b6cfc-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6cfc-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b6cfc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6cfc-129">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="b6cfc-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




