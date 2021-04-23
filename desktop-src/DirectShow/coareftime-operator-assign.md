---
description: Этот оператор назначает новое время ссылки.
ms.assetid: ae6a33ab-f4e0-4f1c-80a0-8a25ee1e9dc5
title: Коарефтиме. operator =-метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f5a051cea555975fd8606c3693d4b7d63cb9ce4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675904"
---
# <a name="coareftimeoperator-method-ctlutilh"></a><span data-ttu-id="1e434-103">Коарефтиме. operator =-метод (Ктлутил. h)</span><span class="sxs-lookup"><span data-stu-id="1e434-103">COARefTime.operator= method (Ctlutil.h)</span></span>

<span data-ttu-id="1e434-104">Этот оператор назначает новое время ссылки.</span><span class="sxs-lookup"><span data-stu-id="1e434-104">This operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e434-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e434-105">Syntax</span></span>


```C++
COARefTime& operator=(
  [ref] const double &rd
);
```



## <a name="parameters"></a><span data-ttu-id="1e434-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e434-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e434-107">*RD* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="1e434-107">*rd* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="1e434-108">Ссылка на значение **Double** , указывающее новое время ссылки в секундах.</span><span class="sxs-lookup"><span data-stu-id="1e434-108">Reference to a **double** value that specifies the new reference time in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e434-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e434-109">Return value</span></span>

<span data-ttu-id="1e434-110">Возвращает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="1e434-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e434-111">Требования</span><span class="sxs-lookup"><span data-stu-id="1e434-111">Requirements</span></span>



| <span data-ttu-id="1e434-112">Требование</span><span class="sxs-lookup"><span data-stu-id="1e434-112">Requirement</span></span> | <span data-ttu-id="1e434-113">Значение</span><span class="sxs-lookup"><span data-stu-id="1e434-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e434-114">Header</span><span class="sxs-lookup"><span data-stu-id="1e434-114">Header</span></span><br/>  | <dl> <span data-ttu-id="1e434-115"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e434-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1e434-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1e434-116">Library</span></span><br/> | <dl> <span data-ttu-id="1e434-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1e434-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e434-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e434-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e434-119">**Класс Коарефтиме**</span><span class="sxs-lookup"><span data-stu-id="1e434-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




