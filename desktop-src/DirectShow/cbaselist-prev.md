---
description: Предыдущий метод извлекает предыдущее расположение в списке.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: Метод Кбаселист. PREV (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03c35a89754b27aa67a5bba33ee694433d74c0fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657386"
---
# <a name="cbaselistprev-method"></a><span data-ttu-id="4b5e9-103">Кбаселист. prev, метод</span><span class="sxs-lookup"><span data-stu-id="4b5e9-103">CBaseList.Prev method</span></span>

<span data-ttu-id="4b5e9-104">`Prev`Метод извлекает предыдущее расположение в списке.</span><span class="sxs-lookup"><span data-stu-id="4b5e9-104">The `Prev` method retrieves the previous position in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b5e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b5e9-105">Syntax</span></span>


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="4b5e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b5e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b5e9-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="4b5e9-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="4b5e9-108">Значение расположения.</span><span class="sxs-lookup"><span data-stu-id="4b5e9-108">POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b5e9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b5e9-109">Return value</span></span>

<span data-ttu-id="4b5e9-110">Возвращает индикатор положения, предшествующий положению, указанному в *POS*.</span><span class="sxs-lookup"><span data-stu-id="4b5e9-110">Returns the position indicator that is previous to the position specified in *pos*.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b5e9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b5e9-111">Remarks</span></span>

<span data-ttu-id="4b5e9-112">Если *POS* является первой позицией в списке, метод возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4b5e9-112">If *pos* is the first position in the list, the method returns **NULL**.</span></span> <span data-ttu-id="4b5e9-113">Если *POS* имеет **значение NULL**, метод возвращает последнюю положение в списке.</span><span class="sxs-lookup"><span data-stu-id="4b5e9-113">If *pos* is **NULL**, the method returns the last position in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b5e9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4b5e9-114">Requirements</span></span>



| <span data-ttu-id="4b5e9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4b5e9-115">Requirement</span></span> | <span data-ttu-id="4b5e9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4b5e9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b5e9-117">Header</span><span class="sxs-lookup"><span data-stu-id="4b5e9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4b5e9-118"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b5e9-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4b5e9-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4b5e9-119">Library</span></span><br/> | <dl> <span data-ttu-id="4b5e9-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4b5e9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b5e9-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b5e9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b5e9-122">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="4b5e9-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




