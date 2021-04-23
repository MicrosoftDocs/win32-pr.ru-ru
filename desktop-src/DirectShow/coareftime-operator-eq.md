---
description: Этот оператор проверяет равенство между двумя временами ссылки.
ms.assetid: a265f7c6-8334-4bb3-8cb7-c7918ebdf97a
title: Коарефтиме. operator = = метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04b19f7b75be840a293920b36fe5ab63d30520d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679977"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="89457-103">Коарефтиме. operator = = метод</span><span class="sxs-lookup"><span data-stu-id="89457-103">COARefTime.operator== method</span></span>

<span data-ttu-id="89457-104">Этот оператор проверяет равенство между двумя временами ссылки.</span><span class="sxs-lookup"><span data-stu-id="89457-104">This operator tests for equality between two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="89457-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89457-105">Syntax</span></span>


```C++
BOOL operator==(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="89457-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="89457-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89457-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="89457-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="89457-108">Ссылка на объект **коарефтиме** для сравнения.</span><span class="sxs-lookup"><span data-stu-id="89457-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89457-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89457-109">Return value</span></span>

<span data-ttu-id="89457-110">Возвращает **значение true** , если два объекта равны.</span><span class="sxs-lookup"><span data-stu-id="89457-110">Returns **TRUE** if the two objects are equal.</span></span> <span data-ttu-id="89457-111">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="89457-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="89457-112">Требования</span><span class="sxs-lookup"><span data-stu-id="89457-112">Requirements</span></span>



| <span data-ttu-id="89457-113">Требование</span><span class="sxs-lookup"><span data-stu-id="89457-113">Requirement</span></span> | <span data-ttu-id="89457-114">Значение</span><span class="sxs-lookup"><span data-stu-id="89457-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89457-115">Header</span><span class="sxs-lookup"><span data-stu-id="89457-115">Header</span></span><br/>  | <dl> <span data-ttu-id="89457-116"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89457-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="89457-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="89457-117">Library</span></span><br/> | <dl> <span data-ttu-id="89457-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="89457-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89457-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89457-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89457-120">**Класс Коарефтиме**</span><span class="sxs-lookup"><span data-stu-id="89457-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




