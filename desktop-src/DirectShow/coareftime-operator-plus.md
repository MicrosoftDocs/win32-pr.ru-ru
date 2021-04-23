---
description: Этот оператор добавляет два времени ссылки.
ms.assetid: 4dfc087a-ec4f-4a8a-8bd4-4da9e1699bcd
title: Метод Коарефтиме. operator + (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a6f5019c61d4c1baec47652db8842aa5085b675
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675912"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="87ddf-103">Коарефтиме. operator +, метод</span><span class="sxs-lookup"><span data-stu-id="87ddf-103">COARefTime.operator+ method</span></span>

<span data-ttu-id="87ddf-104">Этот оператор добавляет два времени ссылки.</span><span class="sxs-lookup"><span data-stu-id="87ddf-104">This operator adds two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ddf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87ddf-105">Syntax</span></span>


```C++
COARefTime operator+(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="87ddf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87ddf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87ddf-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="87ddf-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="87ddf-108">Ссылка на добавляемый объект **коарефтиме** .</span><span class="sxs-lookup"><span data-stu-id="87ddf-108">Reference to the **COARefTime** object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87ddf-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87ddf-109">Return value</span></span>

<span data-ttu-id="87ddf-110">Возвращает новый объект **коарефтиме** , равный сумме времени ссылки.</span><span class="sxs-lookup"><span data-stu-id="87ddf-110">Returns a new **COARefTime** object equal to the sum of the reference times.</span></span>

## <a name="requirements"></a><span data-ttu-id="87ddf-111">Требования</span><span class="sxs-lookup"><span data-stu-id="87ddf-111">Requirements</span></span>



| <span data-ttu-id="87ddf-112">Требование</span><span class="sxs-lookup"><span data-stu-id="87ddf-112">Requirement</span></span> | <span data-ttu-id="87ddf-113">Значение</span><span class="sxs-lookup"><span data-stu-id="87ddf-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87ddf-114">Header</span><span class="sxs-lookup"><span data-stu-id="87ddf-114">Header</span></span><br/>  | <dl> <span data-ttu-id="87ddf-115"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87ddf-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="87ddf-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="87ddf-116">Library</span></span><br/> | <dl> <span data-ttu-id="87ddf-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="87ddf-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87ddf-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87ddf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87ddf-119">**Класс Коарефтиме**</span><span class="sxs-lookup"><span data-stu-id="87ddf-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




