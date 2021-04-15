---
description: Оператор ссылки \_ time () приводит объект к ссылочному \_ типу данных времени.
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: Метод REFERENCE_TIME Крефтиме. operator (Рефтиме. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675711"
---
# <a name="creftimeoperator-reference_time-method"></a><span data-ttu-id="20b80-103">Метод времени ссылки Крефтиме. operator \_</span><span class="sxs-lookup"><span data-stu-id="20b80-103">CRefTime.operator REFERENCE\_TIME method</span></span>

<span data-ttu-id="20b80-104">`REFERENCE_TIME()`Оператор приводит объект к ссылочному типу данных [**\_ времени**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="20b80-104">The `REFERENCE_TIME()` operator casts the object to a [**REFERENCE\_TIME**](reference-time.md) data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="20b80-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20b80-105">Syntax</span></span>


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a><span data-ttu-id="20b80-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="20b80-106">Parameters</span></span>

<span data-ttu-id="20b80-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="20b80-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20b80-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20b80-108">Return value</span></span>

<span data-ttu-id="20b80-109">Возвращает значение [**крефтиме:: m \_ time**](creftime-m-time.md).</span><span class="sxs-lookup"><span data-stu-id="20b80-109">Returns the value of [**CRefTime::m\_time**](creftime-m-time.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="20b80-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20b80-110">Remarks</span></span>

<span data-ttu-id="20b80-111">В следующем примере показано, как использовать этот оператор приведения:</span><span class="sxs-lookup"><span data-stu-id="20b80-111">The following example shows how to use this cast operator:</span></span>


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a><span data-ttu-id="20b80-112">Требования</span><span class="sxs-lookup"><span data-stu-id="20b80-112">Requirements</span></span>



| <span data-ttu-id="20b80-113">Требование</span><span class="sxs-lookup"><span data-stu-id="20b80-113">Requirement</span></span> | <span data-ttu-id="20b80-114">Значение</span><span class="sxs-lookup"><span data-stu-id="20b80-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20b80-115">Header</span><span class="sxs-lookup"><span data-stu-id="20b80-115">Header</span></span><br/>  | <dl> <span data-ttu-id="20b80-116"><dt>Рефтиме. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20b80-116"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="20b80-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="20b80-117">Library</span></span><br/> | <dl> <span data-ttu-id="20b80-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="20b80-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




