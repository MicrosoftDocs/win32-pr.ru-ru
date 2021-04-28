---
description: Кмедиаевент. Жеттипеинфокаунт, метод возвращает количество интерфейсов типа данных, предоставленных объектом.
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: Кмедиаевент. Жеттипеинфокаунт, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9402ad973a08afed4d338cfdc7b5df7fb14b9f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099122"
---
# <a name="cmediaeventgettypeinfocount-method"></a><span data-ttu-id="2dc37-103">Кмедиаевент. Жеттипеинфокаунт, метод</span><span class="sxs-lookup"><span data-stu-id="2dc37-103">CMediaEvent.GetTypeInfoCount method</span></span>

<span data-ttu-id="2dc37-104">Извлекает количество интерфейсов типа данных, предоставленных объектом.</span><span class="sxs-lookup"><span data-stu-id="2dc37-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dc37-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2dc37-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="2dc37-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2dc37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dc37-107">*пктинфо*</span><span class="sxs-lookup"><span data-stu-id="2dc37-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="2dc37-108">Указатель на число интерфейсов типа данных, предоставляемых объектом.</span><span class="sxs-lookup"><span data-stu-id="2dc37-108">Pointer to number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="2dc37-109">Если объект предоставляет сведения о типе, это число равно 1; в противном случае число равно 0.</span><span class="sxs-lookup"><span data-stu-id="2dc37-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dc37-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2dc37-110">Return value</span></span>

<span data-ttu-id="2dc37-111">Возвращает \_ указатель E, если *пктинфо* является недопустимым; в противном случае возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2dc37-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dc37-112">Требования</span><span class="sxs-lookup"><span data-stu-id="2dc37-112">Requirements</span></span>



| <span data-ttu-id="2dc37-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2dc37-113">Requirement</span></span> | <span data-ttu-id="2dc37-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2dc37-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc37-115">Header</span><span class="sxs-lookup"><span data-stu-id="2dc37-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2dc37-116"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2dc37-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2dc37-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2dc37-117">Library</span></span><br/> | <dl> <span data-ttu-id="2dc37-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2dc37-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dc37-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2dc37-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dc37-120">**Класс Кмедиаевент**</span><span class="sxs-lookup"><span data-stu-id="2dc37-120">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




