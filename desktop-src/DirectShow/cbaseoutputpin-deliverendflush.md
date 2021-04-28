---
description: Кбасеаутпутпин. Деливерендфлуш, метод Деливерендфлуш запрашивает подключенный входной ПИН-код для завершения операции очистки.
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: Кбасеаутпутпин. Деливерендфлуш, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f3fd5c1bc686ee5c0b4ff0cd1285a5114b93049
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096182"
---
# <a name="cbaseoutputpindeliverendflush-method"></a><span data-ttu-id="def8d-103">Кбасеаутпутпин. Деливерендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="def8d-103">CBaseOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="def8d-104">`DeliverEndFlush`Метод запрашивает подключенный входной ПИН-код для завершения операции очистки.</span><span class="sxs-lookup"><span data-stu-id="def8d-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="def8d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="def8d-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="def8d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="def8d-106">Parameters</span></span>

<span data-ttu-id="def8d-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="def8d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="def8d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="def8d-108">Return value</span></span>

<span data-ttu-id="def8d-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="def8d-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="def8d-110">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="def8d-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="def8d-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="def8d-111">Return code</span></span>                                                                                           | <span data-ttu-id="def8d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="def8d-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="def8d-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="def8d-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="def8d-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="def8d-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="def8d-115"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="def8d-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="def8d-116">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="def8d-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="def8d-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="def8d-117">Remarks</span></span>

<span data-ttu-id="def8d-118">Этот метод вызывает метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="def8d-118">This method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="def8d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="def8d-119">Requirements</span></span>



| <span data-ttu-id="def8d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="def8d-120">Requirement</span></span> | <span data-ttu-id="def8d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="def8d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="def8d-122">Header</span><span class="sxs-lookup"><span data-stu-id="def8d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="def8d-123"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="def8d-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="def8d-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="def8d-124">Library</span></span><br/> | <dl> <span data-ttu-id="def8d-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="def8d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="def8d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="def8d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def8d-127">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="def8d-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




