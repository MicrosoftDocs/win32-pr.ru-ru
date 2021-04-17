---
description: Этот оператор проверяет, что одно время ссылки меньше или равно другому.
ms.assetid: ae7449b7-d319-4e76-892f-0f9ae63ddf94
title: Коарефтиме. operator>= метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69b345f42c854e939c21a028827889a03e0ce735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675851"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="e1cdc-103">Коарефтиме. operator>= метод</span><span class="sxs-lookup"><span data-stu-id="e1cdc-103">COARefTime.operator>= method</span></span>

<span data-ttu-id="e1cdc-104">Этот оператор проверяет, что одно время ссылки меньше или равно другому.</span><span class="sxs-lookup"><span data-stu-id="e1cdc-104">This operator tests if one reference time is less than or equal to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1cdc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1cdc-105">Syntax</span></span>


```C++
BOOL operator>=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="e1cdc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1cdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1cdc-107">*RT* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="e1cdc-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e1cdc-108">Ссылка на объект **коарефтиме** для сравнения.</span><span class="sxs-lookup"><span data-stu-id="e1cdc-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1cdc-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1cdc-109">Return value</span></span>

<span data-ttu-id="e1cdc-110">Возвращает **значение true** , если этот объект меньше или равен *RT*.</span><span class="sxs-lookup"><span data-stu-id="e1cdc-110">Returns **TRUE** if this object is less than or equal to *rt*.</span></span> <span data-ttu-id="e1cdc-111">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="e1cdc-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1cdc-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e1cdc-112">Requirements</span></span>



| <span data-ttu-id="e1cdc-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e1cdc-113">Requirement</span></span> | <span data-ttu-id="e1cdc-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e1cdc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1cdc-115">Header</span><span class="sxs-lookup"><span data-stu-id="e1cdc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e1cdc-116"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1cdc-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e1cdc-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e1cdc-117">Library</span></span><br/> | <dl> <span data-ttu-id="e1cdc-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e1cdc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1cdc-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1cdc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1cdc-120">**Класс Коарефтиме**</span><span class="sxs-lookup"><span data-stu-id="e1cdc-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




