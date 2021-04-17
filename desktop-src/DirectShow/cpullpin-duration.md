---
description: Метод Duration извлекает длительность потока.
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: Метод Кпуллпин. Duration (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecd05478f67934368aa6d1de84ae32a209ddcad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679651"
---
# <a name="cpullpinduration-method"></a><span data-ttu-id="284b0-103">Кпуллпин. Duration, метод</span><span class="sxs-lookup"><span data-stu-id="284b0-103">CPullPin.Duration method</span></span>

<span data-ttu-id="284b0-104">`Duration`Метод получает длительность потока.</span><span class="sxs-lookup"><span data-stu-id="284b0-104">The `Duration` method retrieves the duration of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="284b0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="284b0-105">Syntax</span></span>


```C++
HRESULT Duration(
   REFERENCE_TIME *ptDuration
);
```



## <a name="parameters"></a><span data-ttu-id="284b0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="284b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="284b0-107">*птдуратион*</span><span class="sxs-lookup"><span data-stu-id="284b0-107">*ptDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="284b0-108">Указатель на переменную, которая получает длительность, в байтах, умноженную на 10 000 000.</span><span class="sxs-lookup"><span data-stu-id="284b0-108">Pointer to a variable that receives the duration, in bytes multiplied by 10,000,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="284b0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="284b0-109">Return value</span></span>

<span data-ttu-id="284b0-110">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="284b0-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="284b0-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="284b0-111">Remarks</span></span>

<span data-ttu-id="284b0-112">Длительность не определена до вызова метода [**кпуллпин:: Connect**](cpullpin-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="284b0-112">The duration is indeterminate until the [**CPullPin::Connect**](cpullpin-connect.md) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="284b0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="284b0-113">Requirements</span></span>



| <span data-ttu-id="284b0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="284b0-114">Requirement</span></span> | <span data-ttu-id="284b0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="284b0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="284b0-116">Header</span><span class="sxs-lookup"><span data-stu-id="284b0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="284b0-117"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="284b0-117"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="284b0-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="284b0-118">Library</span></span><br/> | <dl> <span data-ttu-id="284b0-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="284b0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="284b0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="284b0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="284b0-121">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="284b0-121">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




