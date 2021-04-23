---
description: Метод Деливербегинфлуш запрашивает подключенный входной ПИН-код для начала операции очистки.
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: Кбасеаутпутпин. Деливербегинфлуш, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dad764ceaa6cc57c8c5b7ee288859926b6c63f02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657919"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a><span data-ttu-id="3407c-103">Кбасеаутпутпин. Деливербегинфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="3407c-103">CBaseOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="3407c-104">`DeliverBeginFlush`Метод запрашивает подключенный входной ПИН-код для начала операции очистки.</span><span class="sxs-lookup"><span data-stu-id="3407c-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3407c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3407c-105">Syntax</span></span>


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="3407c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3407c-106">Parameters</span></span>

<span data-ttu-id="3407c-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3407c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3407c-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3407c-108">Return value</span></span>

<span data-ttu-id="3407c-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3407c-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3407c-110">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3407c-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="3407c-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3407c-111">Return code</span></span>                                                                                           | <span data-ttu-id="3407c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="3407c-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3407c-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3407c-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="3407c-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="3407c-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="3407c-115"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="3407c-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="3407c-116">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="3407c-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3407c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3407c-117">Remarks</span></span>

<span data-ttu-id="3407c-118">Этот метод вызывает метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="3407c-118">This method calls the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="3407c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3407c-119">Requirements</span></span>



| <span data-ttu-id="3407c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3407c-120">Requirement</span></span> | <span data-ttu-id="3407c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3407c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3407c-122">Header</span><span class="sxs-lookup"><span data-stu-id="3407c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3407c-123"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3407c-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3407c-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3407c-124">Library</span></span><br/> | <dl> <span data-ttu-id="3407c-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="3407c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3407c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3407c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3407c-127">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="3407c-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




