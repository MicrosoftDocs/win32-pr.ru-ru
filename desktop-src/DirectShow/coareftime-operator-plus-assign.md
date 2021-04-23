---
description: Этот оператор добавляет два значения времени ссылки и присваивает этому объекту результат.
ms.assetid: 6d29014b-0e31-497e-8326-e3fefc022227
title: Метод Коарефтиме. operator + = (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a03d9e98c3c2f2ca09c3f90f2cb0867d976e02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675913"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="ad4ec-103">Коарефтиме. operator + = метод</span><span class="sxs-lookup"><span data-stu-id="ad4ec-103">COARefTime.operator+= method</span></span>

<span data-ttu-id="ad4ec-104">Этот оператор добавляет два значения времени ссылки и присваивает этому объекту результат.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-104">This operator adds two reference times, and sets this object to the result.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad4ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad4ec-105">Syntax</span></span>


```C++
COARefTime& operator+=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="ad4ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad4ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad4ec-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="ad4ec-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ad4ec-108">Ссылка на добавляемый объект **коарефтиме** .</span><span class="sxs-lookup"><span data-stu-id="ad4ec-108">Reference to the **COARefTime** object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad4ec-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad4ec-109">Return value</span></span>

<span data-ttu-id="ad4ec-110">Возвращает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="ad4ec-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad4ec-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ad4ec-111">Requirements</span></span>



| <span data-ttu-id="ad4ec-112">Требование</span><span class="sxs-lookup"><span data-stu-id="ad4ec-112">Requirement</span></span> | <span data-ttu-id="ad4ec-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ad4ec-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad4ec-114">Header</span><span class="sxs-lookup"><span data-stu-id="ad4ec-114">Header</span></span><br/>  | <dl> <span data-ttu-id="ad4ec-115"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad4ec-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ad4ec-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ad4ec-116">Library</span></span><br/> | <dl> <span data-ttu-id="ad4ec-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ad4ec-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad4ec-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad4ec-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad4ec-119">**Класс Коарефтиме**</span><span class="sxs-lookup"><span data-stu-id="ad4ec-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




