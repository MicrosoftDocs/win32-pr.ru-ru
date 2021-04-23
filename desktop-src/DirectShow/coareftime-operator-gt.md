---
description: Этот оператор проверяет, что одно время ссылки больше другого.
ms.assetid: db281040-9bcf-41fc-95b4-5481ffc5061f
title: Метод> Коарефтиме. operator (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c796bd5194c5bdb2dcbe260b803274962f81347
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669387"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="153ee-103">Коарефтиме. operator> метод</span><span class="sxs-lookup"><span data-stu-id="153ee-103">COARefTime.operator> method</span></span>

<span data-ttu-id="153ee-104">Этот оператор проверяет, что одно время ссылки больше другого.</span><span class="sxs-lookup"><span data-stu-id="153ee-104">This operator tests if one reference time is greater than another.</span></span>

## <a name="syntax"></a><span data-ttu-id="153ee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="153ee-105">Syntax</span></span>


```C++
BOOL operator>(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="153ee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="153ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="153ee-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="153ee-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="153ee-108">Ссылка на объект **коарефтиме** для сравнения.</span><span class="sxs-lookup"><span data-stu-id="153ee-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="153ee-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="153ee-109">Return value</span></span>

<span data-ttu-id="153ee-110">Возвращает **значение true** , если этот объект строго больше *RT*.</span><span class="sxs-lookup"><span data-stu-id="153ee-110">Returns **TRUE** if this object is strictly greater than *rt*.</span></span> <span data-ttu-id="153ee-111">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="153ee-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="153ee-112">Требования</span><span class="sxs-lookup"><span data-stu-id="153ee-112">Requirements</span></span>



| <span data-ttu-id="153ee-113">Требование</span><span class="sxs-lookup"><span data-stu-id="153ee-113">Requirement</span></span> | <span data-ttu-id="153ee-114">Значение</span><span class="sxs-lookup"><span data-stu-id="153ee-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="153ee-115">Header</span><span class="sxs-lookup"><span data-stu-id="153ee-115">Header</span></span><br/>  | <dl> <span data-ttu-id="153ee-116"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="153ee-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="153ee-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="153ee-117">Library</span></span><br/> | <dl> <span data-ttu-id="153ee-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="153ee-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="153ee-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="153ee-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="153ee-120">**Класс Коарефтиме**</span><span class="sxs-lookup"><span data-stu-id="153ee-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




