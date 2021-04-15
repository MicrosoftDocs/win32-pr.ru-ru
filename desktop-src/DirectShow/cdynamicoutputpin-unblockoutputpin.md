---
description: Метод Унблоккаутпутпин разблокирует ПИН-код. Если ПИН-код разблокирован, он может доставлять образцы, изменять формат вывода и повторно подключаться к нему.
ms.assetid: ea6e6312-8c7f-44db-ac7f-165dc45dec23
title: Кдинамикаутпутпин. Унблоккаутпутпин, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.UnblockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bcde3ccad01e19f3802e2cd19f0f6b873380ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669129"
---
# <a name="cdynamicoutputpinunblockoutputpin-method"></a><span data-ttu-id="5dae0-104">Кдинамикаутпутпин. Унблоккаутпутпин, метод</span><span class="sxs-lookup"><span data-stu-id="5dae0-104">CDynamicOutputPin.UnblockOutputPin method</span></span>

<span data-ttu-id="5dae0-105">`UnblockOutputPin`Метод разблокирует ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="5dae0-105">The `UnblockOutputPin` method unblocks the pin.</span></span> <span data-ttu-id="5dae0-106">Если ПИН-код разблокирован, он может доставлять образцы, изменять формат вывода и повторно подключаться к нему.</span><span class="sxs-lookup"><span data-stu-id="5dae0-106">When the pin is unblocked, it can deliver samples, change its output format, and reconnect itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dae0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dae0-107">Syntax</span></span>


```C++
HRESULT UnblockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="5dae0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5dae0-108">Parameters</span></span>

<span data-ttu-id="5dae0-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5dae0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5dae0-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5dae0-110">Return value</span></span>

<span data-ttu-id="5dae0-111">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5dae0-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="5dae0-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5dae0-112">Return code</span></span>                                                                             | <span data-ttu-id="5dae0-113">Описание</span><span class="sxs-lookup"><span data-stu-id="5dae0-113">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5dae0-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="5dae0-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="5dae0-115">ПИН-код уже разблокирован.</span><span class="sxs-lookup"><span data-stu-id="5dae0-115">Pin was already unblocked.</span></span><br/> |
| <dl> <span data-ttu-id="5dae0-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5dae0-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="5dae0-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="5dae0-117">Success.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="5dae0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5dae0-118">Requirements</span></span>



| <span data-ttu-id="5dae0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5dae0-119">Requirement</span></span> | <span data-ttu-id="5dae0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5dae0-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dae0-121">Header</span><span class="sxs-lookup"><span data-stu-id="5dae0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5dae0-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5dae0-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5dae0-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5dae0-123">Library</span></span><br/> | <dl> <span data-ttu-id="5dae0-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5dae0-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dae0-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dae0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dae0-126">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="5dae0-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




