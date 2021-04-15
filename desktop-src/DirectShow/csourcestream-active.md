---
description: 'Активный метод уведомляет ПИН-код о том, что фильтр активен. Этот метод переопределяет метод Кбасепин:: Active. Если ПИН-код подключен, этот метод запускает поток потоковой передачи.'
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: Метод Ксаурцестреам. Active (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a161c82621f29b916e03fbc2e59ec762871940b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688931"
---
# <a name="csourcestreamactive-method"></a><span data-ttu-id="645f8-105">Ксаурцестреам. активный метод</span><span class="sxs-lookup"><span data-stu-id="645f8-105">CSourceStream.Active method</span></span>

<span data-ttu-id="645f8-106">`Active`Метод уведомляет ПИН-код о том, что фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="645f8-106">The `Active` method notifies the pin that the filter is now active.</span></span> <span data-ttu-id="645f8-107">Этот метод переопределяет метод [**кбасепин:: Active**](cbasepin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="645f8-107">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="645f8-108">Если ПИН-код подключен, этот метод запускает поток потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="645f8-108">If the pin is connected, this method starts the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="645f8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="645f8-109">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="645f8-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="645f8-110">Parameters</span></span>

<span data-ttu-id="645f8-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="645f8-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="645f8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="645f8-112">Return value</span></span>

<span data-ttu-id="645f8-113">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="645f8-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="645f8-114">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="645f8-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="645f8-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="645f8-115">Return code</span></span>                                                                             | <span data-ttu-id="645f8-116">Описание</span><span class="sxs-lookup"><span data-stu-id="645f8-116">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="645f8-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="645f8-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="645f8-118">ПИН-код уже активен.</span><span class="sxs-lookup"><span data-stu-id="645f8-118">The pin is already active.</span></span><br/>  |
| <dl> <span data-ttu-id="645f8-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="645f8-119"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="645f8-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="645f8-120">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="645f8-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="645f8-121"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="645f8-122">Не удалось запустить поток.</span><span class="sxs-lookup"><span data-stu-id="645f8-122">Could not start the thread.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="645f8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="645f8-123">Requirements</span></span>



| <span data-ttu-id="645f8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="645f8-124">Requirement</span></span> | <span data-ttu-id="645f8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="645f8-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="645f8-126">Header</span><span class="sxs-lookup"><span data-stu-id="645f8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="645f8-127"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="645f8-127"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="645f8-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="645f8-128">Library</span></span><br/> | <dl> <span data-ttu-id="645f8-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="645f8-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="645f8-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="645f8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="645f8-131">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="645f8-131">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




