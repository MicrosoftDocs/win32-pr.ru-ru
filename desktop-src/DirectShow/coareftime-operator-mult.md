---
description: Этот оператор умножает время ссылки на значение.
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: Метод Коарефтиме. operator * (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator*
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c62a4282f7a43ba3d7ba35daf81530f8b246be32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668917"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="15854-103">Коарефтиме. operator, \* метод</span><span class="sxs-lookup"><span data-stu-id="15854-103">COARefTime.operator\* method</span></span>

<span data-ttu-id="15854-104">Этот оператор умножает время ссылки на значение.</span><span class="sxs-lookup"><span data-stu-id="15854-104">This operator multiplies a reference time by a value.</span></span>

## <a name="syntax"></a><span data-ttu-id="15854-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15854-105">Syntax</span></span>


```C++
COARefTime operator*(
   LONG l
);
```



## <a name="parameters"></a><span data-ttu-id="15854-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="15854-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15854-107">*l*</span><span class="sxs-lookup"><span data-stu-id="15854-107">*l*</span></span> 
</dt> <dd>

<span data-ttu-id="15854-108">Множитель.</span><span class="sxs-lookup"><span data-stu-id="15854-108">Multiplier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15854-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15854-109">Return value</span></span>

<span data-ttu-id="15854-110">Возвращает новый объект **коарефтиме** , равный продукту этого объекта и **l**.</span><span class="sxs-lookup"><span data-stu-id="15854-110">Returns a new **COARefTime** object equal to the product of this object and **l**.</span></span>

## <a name="requirements"></a><span data-ttu-id="15854-111">Требования</span><span class="sxs-lookup"><span data-stu-id="15854-111">Requirements</span></span>



| <span data-ttu-id="15854-112">Требование</span><span class="sxs-lookup"><span data-stu-id="15854-112">Requirement</span></span> | <span data-ttu-id="15854-113">Значение</span><span class="sxs-lookup"><span data-stu-id="15854-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15854-114">Header</span><span class="sxs-lookup"><span data-stu-id="15854-114">Header</span></span><br/>  | <dl> <span data-ttu-id="15854-115"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15854-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="15854-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="15854-116">Library</span></span><br/> | <dl> <span data-ttu-id="15854-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="15854-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15854-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15854-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15854-119">**Класс Коарефтиме**</span><span class="sxs-lookup"><span data-stu-id="15854-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




