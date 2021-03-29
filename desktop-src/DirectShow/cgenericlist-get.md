---
description: Метод Get извлекает элемент в указанной позиции.
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: Метод Кженериклист. Get (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Get
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02af7d57d2219e6eb0506a8ab11521b4cf3570eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668814"
---
# <a name="cgenericlistget-method"></a><span data-ttu-id="c0db7-103">Кженериклист. Get, метод</span><span class="sxs-lookup"><span data-stu-id="c0db7-103">CGenericList.Get method</span></span>

<span data-ttu-id="c0db7-104">`Get`Метод извлекает элемент в указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="c0db7-104">The `Get` method retrieves the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0db7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0db7-105">Syntax</span></span>


```C++
OBJECT* Get(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="c0db7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0db7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0db7-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="c0db7-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="c0db7-108">Индикатор позиции для извлекаемого элемента.</span><span class="sxs-lookup"><span data-stu-id="c0db7-108">Position indicator for the item to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0db7-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0db7-109">Return value</span></span>

<span data-ttu-id="c0db7-110">Возвращает указатель на объект типа **Object** (тип шаблона).</span><span class="sxs-lookup"><span data-stu-id="c0db7-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="c0db7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0db7-111">Remarks</span></span>

<span data-ttu-id="c0db7-112">Если *POS* имеет **значение NULL**, метод возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c0db7-112">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0db7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c0db7-113">Requirements</span></span>



| <span data-ttu-id="c0db7-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c0db7-114">Requirement</span></span> | <span data-ttu-id="c0db7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c0db7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0db7-116">Header</span><span class="sxs-lookup"><span data-stu-id="c0db7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c0db7-117"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0db7-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c0db7-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c0db7-118">Library</span></span><br/> | <dl> <span data-ttu-id="c0db7-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c0db7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0db7-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0db7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0db7-121">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="c0db7-121">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




