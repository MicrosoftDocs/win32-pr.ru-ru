---
description: Метод Жетфрикаунт извлекает количество неиспользуемых выборок мультимедиа.
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: Кбасеаллокатор. Жетфрикаунт, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetFreeCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0538229053b5d47ca1bdc8f30b38a0937e36cb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669135"
---
# <a name="cbaseallocatorgetfreecount-method"></a><span data-ttu-id="41429-103">Кбасеаллокатор. Жетфрикаунт, метод</span><span class="sxs-lookup"><span data-stu-id="41429-103">CBaseAllocator.GetFreeCount method</span></span>

<span data-ttu-id="41429-104">`GetFreeCount`Метод получает количество неиспользуемых выборок мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="41429-104">The `GetFreeCount` method retrieves the number of media samples that are not in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="41429-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41429-105">Syntax</span></span>


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a><span data-ttu-id="41429-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="41429-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41429-107">*плбуфферсфри*</span><span class="sxs-lookup"><span data-stu-id="41429-107">*plBuffersFree*</span></span> 
</dt> <dd>

<span data-ttu-id="41429-108">Адрес переменной, которая получает количество неиспользуемых выборок.</span><span class="sxs-lookup"><span data-stu-id="41429-108">Address of a variable that receives the number of samples that are not in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41429-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41429-109">Return value</span></span>

<span data-ttu-id="41429-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="41429-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="41429-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41429-111">Remarks</span></span>

<span data-ttu-id="41429-112">Этот метод реализует метод [**имемаллокаторкаллбакктемп:: жетфрикаунт**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) .</span><span class="sxs-lookup"><span data-stu-id="41429-112">This method implements the [**IMemAllocatorCallbackTemp::GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) method.</span></span> <span data-ttu-id="41429-113">Распределитель не предоставляет интерфейс Имемаллокаторкаллбакктемп, если в конструкторе Кбасеаллокатор для флага *фенаблерелеасекаллбакк* не задано **значение true** .</span><span class="sxs-lookup"><span data-stu-id="41429-113">The allocator does not expose the IMemAllocatorCallbackTemp interface unless the *fEnableReleaseCallback* flag is set to **TRUE** in the CBaseAllocator constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="41429-114">Требования</span><span class="sxs-lookup"><span data-stu-id="41429-114">Requirements</span></span>



| <span data-ttu-id="41429-115">Требование</span><span class="sxs-lookup"><span data-stu-id="41429-115">Requirement</span></span> | <span data-ttu-id="41429-116">Значение</span><span class="sxs-lookup"><span data-stu-id="41429-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41429-117">Header</span><span class="sxs-lookup"><span data-stu-id="41429-117">Header</span></span><br/>  | <dl> <span data-ttu-id="41429-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41429-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="41429-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="41429-119">Library</span></span><br/> | <dl> <span data-ttu-id="41429-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="41429-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41429-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41429-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41429-122">**Класс Кбасеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="41429-122">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




