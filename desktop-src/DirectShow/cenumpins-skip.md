---
description: 'Метод Skip пропускает указанное число ПИН-кодов в последовательности перечисления. Этот метод реализует метод Иенумпинс:: Skip.'
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: Метод Ценумпинс. Skip (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1865453a89130303f28f338d8b7567e856c64173
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668823"
---
# <a name="cenumpinsskip-method"></a><span data-ttu-id="46481-104">Ценумпинс. Skip, метод</span><span class="sxs-lookup"><span data-stu-id="46481-104">CEnumPins.Skip method</span></span>

<span data-ttu-id="46481-105">`Skip`Метод пропускает указанное число ПИН-кодов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="46481-105">The `Skip` method skips over a specified number of pins in the enumeration sequence.</span></span> <span data-ttu-id="46481-106">Этот метод реализует метод [**иенумпинс:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) .</span><span class="sxs-lookup"><span data-stu-id="46481-106">This method implements the [**IEnumPins::Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="46481-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46481-107">Syntax</span></span>


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a><span data-ttu-id="46481-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="46481-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46481-109">*кпинс*</span><span class="sxs-lookup"><span data-stu-id="46481-109">*cPins*</span></span> 
</dt> <dd>

<span data-ttu-id="46481-110">Число пропущенных контактов.</span><span class="sxs-lookup"><span data-stu-id="46481-110">Number of pins to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46481-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46481-111">Return value</span></span>

<span data-ttu-id="46481-112">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="46481-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="46481-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="46481-113">Return code</span></span>                                                                                                | <span data-ttu-id="46481-114">Описание</span><span class="sxs-lookup"><span data-stu-id="46481-114">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="46481-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="46481-115"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="46481-116">Пропущено после конца последовательности.</span><span class="sxs-lookup"><span data-stu-id="46481-116">Skipped past the end of the sequence.</span></span><br/>                                       |
| <dl> <span data-ttu-id="46481-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="46481-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="46481-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="46481-118">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="46481-119"><dt>**VFW \_ E \_ перечисление не \_ \_ \_ синхронизировано**</dt></span><span class="sxs-lookup"><span data-stu-id="46481-119"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="46481-120">Состояние фильтра изменилось и теперь не согласуется с перечислителем.</span><span class="sxs-lookup"><span data-stu-id="46481-120">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="46481-121">Требования</span><span class="sxs-lookup"><span data-stu-id="46481-121">Requirements</span></span>



| <span data-ttu-id="46481-122">Требование</span><span class="sxs-lookup"><span data-stu-id="46481-122">Requirement</span></span> | <span data-ttu-id="46481-123">Значение</span><span class="sxs-lookup"><span data-stu-id="46481-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46481-124">Header</span><span class="sxs-lookup"><span data-stu-id="46481-124">Header</span></span><br/>  | <dl> <span data-ttu-id="46481-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46481-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="46481-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="46481-126">Library</span></span><br/> | <dl> <span data-ttu-id="46481-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="46481-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46481-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46481-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46481-129">**Класс Ценумпинс**</span><span class="sxs-lookup"><span data-stu-id="46481-129">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




