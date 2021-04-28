---
description: Кбасеаутпутпин. Деливербегинфлуш, метод Деливербегинфлуш запрашивает подключенный входной ПИН-код для начала операции очистки.
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
ms.openlocfilehash: 22dbd2bccf33d9f203d1505106184500b8cae3ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099522"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a><span data-ttu-id="842c7-103">Кбасеаутпутпин. Деливербегинфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="842c7-103">CBaseOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="842c7-104">`DeliverBeginFlush`Метод запрашивает подключенный входной ПИН-код для начала операции очистки.</span><span class="sxs-lookup"><span data-stu-id="842c7-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="842c7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="842c7-105">Syntax</span></span>


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="842c7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="842c7-106">Parameters</span></span>

<span data-ttu-id="842c7-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="842c7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="842c7-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="842c7-108">Return value</span></span>

<span data-ttu-id="842c7-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="842c7-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="842c7-110">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="842c7-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="842c7-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="842c7-111">Return code</span></span>                                                                                           | <span data-ttu-id="842c7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="842c7-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="842c7-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="842c7-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="842c7-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="842c7-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="842c7-115"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="842c7-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="842c7-116">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="842c7-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="842c7-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="842c7-117">Remarks</span></span>

<span data-ttu-id="842c7-118">Этот метод вызывает метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="842c7-118">This method calls the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="842c7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="842c7-119">Requirements</span></span>



| <span data-ttu-id="842c7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="842c7-120">Requirement</span></span> | <span data-ttu-id="842c7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="842c7-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="842c7-122">Header</span><span class="sxs-lookup"><span data-stu-id="842c7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="842c7-123"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="842c7-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="842c7-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="842c7-124">Library</span></span><br/> | <dl> <span data-ttu-id="842c7-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="842c7-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="842c7-126">См. также</span><span class="sxs-lookup"><span data-stu-id="842c7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="842c7-127">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="842c7-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




