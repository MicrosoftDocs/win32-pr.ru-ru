---
description: Метод Деливерендфлуш запрашивает подключенный входной ПИН-код для завершения операции очистки.
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
ms.openlocfilehash: cb9b92947f2452b8755109c4b83cb21afa119461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669178"
---
# <a name="cbaseoutputpindeliverendflush-method"></a><span data-ttu-id="899f4-103">Кбасеаутпутпин. Деливерендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="899f4-103">CBaseOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="899f4-104">`DeliverEndFlush`Метод запрашивает подключенный входной ПИН-код для завершения операции очистки.</span><span class="sxs-lookup"><span data-stu-id="899f4-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="899f4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="899f4-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="899f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="899f4-106">Parameters</span></span>

<span data-ttu-id="899f4-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="899f4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="899f4-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="899f4-108">Return value</span></span>

<span data-ttu-id="899f4-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="899f4-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="899f4-110">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="899f4-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="899f4-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="899f4-111">Return code</span></span>                                                                                           | <span data-ttu-id="899f4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="899f4-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="899f4-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="899f4-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="899f4-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="899f4-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="899f4-115"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="899f4-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="899f4-116">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="899f4-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="899f4-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="899f4-117">Remarks</span></span>

<span data-ttu-id="899f4-118">Этот метод вызывает метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="899f4-118">This method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="899f4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="899f4-119">Requirements</span></span>



| <span data-ttu-id="899f4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="899f4-120">Requirement</span></span> | <span data-ttu-id="899f4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="899f4-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="899f4-122">Header</span><span class="sxs-lookup"><span data-stu-id="899f4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="899f4-123"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="899f4-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="899f4-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="899f4-124">Library</span></span><br/> | <dl> <span data-ttu-id="899f4-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="899f4-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="899f4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="899f4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="899f4-127">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="899f4-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




