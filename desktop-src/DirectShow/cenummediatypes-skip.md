---
description: 'Метод Skip пропускает указанное число типов мультимедиа. Этот метод реализует метод Иенуммедиатипес:: Skip.'
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: Метод Ценуммедиатипес. Skip (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e09217bc45b866cfb08aa2ab0cae5a7a28815fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657588"
---
# <a name="cenummediatypesskip-method"></a><span data-ttu-id="071d1-104">Ценуммедиатипес. Skip, метод</span><span class="sxs-lookup"><span data-stu-id="071d1-104">CEnumMediaTypes.Skip method</span></span>

<span data-ttu-id="071d1-105">`Skip`Метод пропускает указанное число типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="071d1-105">The `Skip` method skips over a specified number of media types.</span></span> <span data-ttu-id="071d1-106">Этот метод реализует метод [**иенуммедиатипес:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) .</span><span class="sxs-lookup"><span data-stu-id="071d1-106">This method implements the [**IEnumMediaTypes::Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="071d1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="071d1-107">Syntax</span></span>


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="071d1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="071d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="071d1-109">*кмедиатипес*</span><span class="sxs-lookup"><span data-stu-id="071d1-109">*cMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="071d1-110">Число пропускаемых типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="071d1-110">Number of media types to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="071d1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="071d1-111">Return value</span></span>

<span data-ttu-id="071d1-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="071d1-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="071d1-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="071d1-113">Return code</span></span>                                                                                                | <span data-ttu-id="071d1-114">Описание</span><span class="sxs-lookup"><span data-stu-id="071d1-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="071d1-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="071d1-115"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="071d1-116">Пропущено после конца последовательности.</span><span class="sxs-lookup"><span data-stu-id="071d1-116">Skipped past the end of the sequence.</span></span><br/>                                    |
| <dl> <span data-ttu-id="071d1-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="071d1-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="071d1-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="071d1-118">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="071d1-119"><dt>**VFW \_ E \_ перечисление не \_ \_ \_ синхронизировано**</dt></span><span class="sxs-lookup"><span data-stu-id="071d1-119"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="071d1-120">Состояние ПИН-кода изменилось и теперь не согласуется с перечислителем.</span><span class="sxs-lookup"><span data-stu-id="071d1-120">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="071d1-121">Требования</span><span class="sxs-lookup"><span data-stu-id="071d1-121">Requirements</span></span>



| <span data-ttu-id="071d1-122">Требование</span><span class="sxs-lookup"><span data-stu-id="071d1-122">Requirement</span></span> | <span data-ttu-id="071d1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="071d1-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="071d1-124">Header</span><span class="sxs-lookup"><span data-stu-id="071d1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="071d1-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="071d1-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="071d1-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="071d1-126">Library</span></span><br/> | <dl> <span data-ttu-id="071d1-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="071d1-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="071d1-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="071d1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="071d1-129">**Класс Ценуммедиатипес**</span><span class="sxs-lookup"><span data-stu-id="071d1-129">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




