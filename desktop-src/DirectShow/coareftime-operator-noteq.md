---
description: Этот оператор проверяет неравенство между двумя временами ссылки.
ms.assetid: c081fff2-d85e-409a-8902-4b2aa2c1fc78
title: Метод Коарефтиме. operator! = (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e93934d7b31715422f2cc091e606b681a57e7f61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668916"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="adb7c-103">Коарефтиме. operator! = метод</span><span class="sxs-lookup"><span data-stu-id="adb7c-103">COARefTime.operator!= method</span></span>

<span data-ttu-id="adb7c-104">Этот оператор проверяет неравенство между двумя временами ссылки.</span><span class="sxs-lookup"><span data-stu-id="adb7c-104">This operator tests for inequality between two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="adb7c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adb7c-105">Syntax</span></span>


```C++
BOOL operator!=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="adb7c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="adb7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adb7c-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="adb7c-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="adb7c-108">Ссылка на объект **коарефтиме** для сравнения.</span><span class="sxs-lookup"><span data-stu-id="adb7c-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adb7c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="adb7c-109">Return value</span></span>

<span data-ttu-id="adb7c-110">Возвращает **значение true** , если два объекта не равны.</span><span class="sxs-lookup"><span data-stu-id="adb7c-110">Returns **TRUE** if the two objects are not equal.</span></span> <span data-ttu-id="adb7c-111">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="adb7c-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="adb7c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="adb7c-112">Requirements</span></span>



| <span data-ttu-id="adb7c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="adb7c-113">Requirement</span></span> | <span data-ttu-id="adb7c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="adb7c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adb7c-115">Header</span><span class="sxs-lookup"><span data-stu-id="adb7c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="adb7c-116"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="adb7c-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="adb7c-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="adb7c-117">Library</span></span><br/> | <dl> <span data-ttu-id="adb7c-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="adb7c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adb7c-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adb7c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adb7c-120">**Класс Коарефтиме**</span><span class="sxs-lookup"><span data-stu-id="adb7c-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




