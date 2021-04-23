---
description: Этот оператор Вычитает одно время ссылки из другого.
ms.assetid: 5691cd76-0d25-45c0-bb58-6668abe1db01
title: Коарефтиме. operator-метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e51ee8aaed69830a498d1d22cebdc3927987f045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665509"
---
# <a name="coareftimeoperator--method"></a><span data-ttu-id="16616-103">Коарефтиме. operator — метод</span><span class="sxs-lookup"><span data-stu-id="16616-103">COARefTime.operator- method</span></span>

<span data-ttu-id="16616-104">Этот оператор Вычитает одно время ссылки из другого.</span><span class="sxs-lookup"><span data-stu-id="16616-104">This operator subtracts one reference time from another.</span></span>

## <a name="syntax"></a><span data-ttu-id="16616-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16616-105">Syntax</span></span>


```C++
COARefTime operator-(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="16616-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="16616-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16616-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="16616-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="16616-108">Ссылка на объект **коарефтиме** для вычитания.</span><span class="sxs-lookup"><span data-stu-id="16616-108">Reference to the **COARefTime** object to subtract.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16616-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16616-109">Return value</span></span>

<span data-ttu-id="16616-110">Возвращает новый объект **коарефтиме** , равный разности времени ссылки.</span><span class="sxs-lookup"><span data-stu-id="16616-110">Returns a new **COARefTime** object equal to the difference of the reference times.</span></span>

## <a name="requirements"></a><span data-ttu-id="16616-111">Требования</span><span class="sxs-lookup"><span data-stu-id="16616-111">Requirements</span></span>



| <span data-ttu-id="16616-112">Требование</span><span class="sxs-lookup"><span data-stu-id="16616-112">Requirement</span></span> | <span data-ttu-id="16616-113">Значение</span><span class="sxs-lookup"><span data-stu-id="16616-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16616-114">Header</span><span class="sxs-lookup"><span data-stu-id="16616-114">Header</span></span><br/>  | <dl> <span data-ttu-id="16616-115"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16616-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="16616-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="16616-116">Library</span></span><br/> | <dl> <span data-ttu-id="16616-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="16616-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16616-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16616-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16616-119">**Класс Коарефтиме**</span><span class="sxs-lookup"><span data-stu-id="16616-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




