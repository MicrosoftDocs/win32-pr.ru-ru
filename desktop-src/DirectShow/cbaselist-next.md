---
description: Следующий метод извлекает следующее расположение в списке.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Метод Кбаселист. Next (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8a09ec91191437fbfb851ce92824b118a5440ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668596"
---
# <a name="cbaselistnext-method"></a><span data-ttu-id="1f2c2-103">Кбаселист. Next, метод</span><span class="sxs-lookup"><span data-stu-id="1f2c2-103">CBaseList.Next method</span></span>

<span data-ttu-id="1f2c2-104">`Next`Метод получает следующую точку в списке.</span><span class="sxs-lookup"><span data-stu-id="1f2c2-104">The `Next` method retrieves the next position in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f2c2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f2c2-105">Syntax</span></span>


```C++
POSITION Next(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="1f2c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f2c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f2c2-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="1f2c2-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="1f2c2-108">Значение расположения.</span><span class="sxs-lookup"><span data-stu-id="1f2c2-108">POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f2c2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f2c2-109">Return value</span></span>

<span data-ttu-id="1f2c2-110">Возвращает индикатор положения, следующий за позицией, заданной в *POS*.</span><span class="sxs-lookup"><span data-stu-id="1f2c2-110">Returns the position indicator that follows the position specified by *pos*.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f2c2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f2c2-111">Remarks</span></span>

<span data-ttu-id="1f2c2-112">Если *POS* является последней позицией в списке, метод возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1f2c2-112">If *pos* is the last position in the list, the method returns **NULL**.</span></span> <span data-ttu-id="1f2c2-113">Если *POS* имеет **значение NULL**, метод возвращает первую точку в списке.</span><span class="sxs-lookup"><span data-stu-id="1f2c2-113">If *pos* is **NULL**, the method returns the first position in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f2c2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1f2c2-114">Requirements</span></span>



| <span data-ttu-id="1f2c2-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1f2c2-115">Requirement</span></span> | <span data-ttu-id="1f2c2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1f2c2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f2c2-117">Header</span><span class="sxs-lookup"><span data-stu-id="1f2c2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1f2c2-118"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f2c2-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1f2c2-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1f2c2-119">Library</span></span><br/> | <dl> <span data-ttu-id="1f2c2-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1f2c2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f2c2-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f2c2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f2c2-122">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="1f2c2-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




