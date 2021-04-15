---
description: Этот оператор проверяет, меньше ли одно время ссылки, чем другое.
ms.assetid: 709fb861-a836-4a20-8c93-c0e8ab79f377
title: Метод< Коарефтиме. operator (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c61403b959f8b5ee19e9ba0d9cd0ab4db54c124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668922"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="a7264-103">Коарефтиме. operator< метод</span><span class="sxs-lookup"><span data-stu-id="a7264-103">COARefTime.operator< method</span></span>

<span data-ttu-id="a7264-104">Этот оператор проверяет, меньше ли одно время ссылки, чем другое.</span><span class="sxs-lookup"><span data-stu-id="a7264-104">This operator tests if one reference time is less than another.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7264-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7264-105">Syntax</span></span>


```C++
BOOL operator<(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="a7264-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7264-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7264-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="a7264-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a7264-108">Ссылка на объект **коарефтиме** для сравнения.</span><span class="sxs-lookup"><span data-stu-id="a7264-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7264-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7264-109">Return value</span></span>

<span data-ttu-id="a7264-110">Возвращает **значение true** , если этот объект строго меньше *RT*.</span><span class="sxs-lookup"><span data-stu-id="a7264-110">Returns **TRUE** if this object is strictly less than *rt*.</span></span> <span data-ttu-id="a7264-111">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a7264-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7264-112">Требования</span><span class="sxs-lookup"><span data-stu-id="a7264-112">Requirements</span></span>



| <span data-ttu-id="a7264-113">Требование</span><span class="sxs-lookup"><span data-stu-id="a7264-113">Requirement</span></span> | <span data-ttu-id="a7264-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a7264-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7264-115">Header</span><span class="sxs-lookup"><span data-stu-id="a7264-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a7264-116"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7264-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a7264-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a7264-117">Library</span></span><br/> | <dl> <span data-ttu-id="a7264-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a7264-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7264-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7264-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7264-120">**Класс Коарефтиме**</span><span class="sxs-lookup"><span data-stu-id="a7264-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




