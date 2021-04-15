---
description: Этот оператор делит время ссылки на значение.
ms.assetid: fb2e2a4b-dc0b-42e3-86c7-8aa2c60daedc
title: Коарефтиме. operator/метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator/
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e1e4d7b7adb881ac11988a2d2c46946ff6cddcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668898"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="fd23c-103">Коарефтиме. operator/-метод</span><span class="sxs-lookup"><span data-stu-id="fd23c-103">COARefTime.operator/ method</span></span>

<span data-ttu-id="fd23c-104">Этот оператор делит время ссылки на значение.</span><span class="sxs-lookup"><span data-stu-id="fd23c-104">This operator divides a reference time by a value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd23c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd23c-105">Syntax</span></span>


```C++
COARefTime operator/(
   LONG l
);
```



## <a name="parameters"></a><span data-ttu-id="fd23c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd23c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd23c-107">*l*</span><span class="sxs-lookup"><span data-stu-id="fd23c-107">*l*</span></span> 
</dt> <dd>

<span data-ttu-id="fd23c-108">Равн.</span><span class="sxs-lookup"><span data-stu-id="fd23c-108">Divisor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd23c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd23c-109">Return value</span></span>

<span data-ttu-id="fd23c-110">Возвращает новый объект **коарефтиме** , равный частям данного объекта и **l**.</span><span class="sxs-lookup"><span data-stu-id="fd23c-110">Returns a new **COARefTime** object equal to the quotient of this object and **l**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd23c-111">Требования</span><span class="sxs-lookup"><span data-stu-id="fd23c-111">Requirements</span></span>



| <span data-ttu-id="fd23c-112">Требование</span><span class="sxs-lookup"><span data-stu-id="fd23c-112">Requirement</span></span> | <span data-ttu-id="fd23c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="fd23c-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd23c-114">Header</span><span class="sxs-lookup"><span data-stu-id="fd23c-114">Header</span></span><br/>  | <dl> <span data-ttu-id="fd23c-115"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd23c-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fd23c-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fd23c-116">Library</span></span><br/> | <dl> <span data-ttu-id="fd23c-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fd23c-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd23c-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd23c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd23c-119">**Класс Коарефтиме**</span><span class="sxs-lookup"><span data-stu-id="fd23c-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




