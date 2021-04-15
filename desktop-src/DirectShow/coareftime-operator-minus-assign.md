---
description: Этот оператор Вычитает одно время ссылки из другого и присваивает этому объекту результат.
ms.assetid: 573b6f6b-7634-4e78-872c-f869b59a75e2
title: Метод Коарефтиме. operator-= (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 29afc98da01351f63df45997b8cc338e17a1234c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668920"
---
# <a name="coareftimeoperator--method"></a><span data-ttu-id="09c99-103">Коарефтиме. operator-= метод</span><span class="sxs-lookup"><span data-stu-id="09c99-103">COARefTime.operator-= method</span></span>

<span data-ttu-id="09c99-104">Этот оператор Вычитает одно время ссылки из другого и присваивает этому объекту результат.</span><span class="sxs-lookup"><span data-stu-id="09c99-104">This operator subtracts one reference time from another, and sets this object to the result.</span></span>

## <a name="syntax"></a><span data-ttu-id="09c99-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09c99-105">Syntax</span></span>


```C++
COARefTime& operator-=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="09c99-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="09c99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09c99-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="09c99-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="09c99-108">Ссылка на объект **коарефтиме** для вычитания.</span><span class="sxs-lookup"><span data-stu-id="09c99-108">Reference to the **COARefTime** object to subtract.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09c99-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09c99-109">Return value</span></span>

<span data-ttu-id="09c99-110">Возвращает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="09c99-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="09c99-111">Требования</span><span class="sxs-lookup"><span data-stu-id="09c99-111">Requirements</span></span>



| <span data-ttu-id="09c99-112">Требование</span><span class="sxs-lookup"><span data-stu-id="09c99-112">Requirement</span></span> | <span data-ttu-id="09c99-113">Значение</span><span class="sxs-lookup"><span data-stu-id="09c99-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09c99-114">Header</span><span class="sxs-lookup"><span data-stu-id="09c99-114">Header</span></span><br/>  | <dl> <span data-ttu-id="09c99-115"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09c99-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="09c99-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="09c99-116">Library</span></span><br/> | <dl> <span data-ttu-id="09c99-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="09c99-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09c99-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09c99-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09c99-119">**Класс Коарефтиме**</span><span class="sxs-lookup"><span data-stu-id="09c99-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




