---
description: Метод Чеккстреаминг определяет, может ли ПИН-код принимать выборки.
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: Ктрансформинпутпин. Чеккстреаминг, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e5c49a00054547193e3f492f0731f77af8331a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657408"
---
# <a name="ctransforminputpincheckstreaming-method"></a><span data-ttu-id="74c1d-103">Ктрансформинпутпин. Чеккстреаминг, метод</span><span class="sxs-lookup"><span data-stu-id="74c1d-103">CTransformInputPin.CheckStreaming method</span></span>

<span data-ttu-id="74c1d-104">`CheckStreaming`Метод определяет, может ли ПИН-код принимать выборки.</span><span class="sxs-lookup"><span data-stu-id="74c1d-104">The `CheckStreaming` method determines whether the pin can accept samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c1d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74c1d-105">Syntax</span></span>


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a><span data-ttu-id="74c1d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="74c1d-106">Parameters</span></span>

<span data-ttu-id="74c1d-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="74c1d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74c1d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74c1d-108">Return value</span></span>

<span data-ttu-id="74c1d-109">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="74c1d-109">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="74c1d-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="74c1d-110">Return code</span></span>                                                                                           | <span data-ttu-id="74c1d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="74c1d-111">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="74c1d-112"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="74c1d-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="74c1d-113">Успешно.</span><span class="sxs-lookup"><span data-stu-id="74c1d-113">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="74c1d-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="74c1d-114"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="74c1d-115">ПИН-код в данный момент очищается.</span><span class="sxs-lookup"><span data-stu-id="74c1d-115">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="74c1d-116"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="74c1d-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="74c1d-117">Выходной ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="74c1d-117">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="74c1d-118"><dt>**\_ \_ ошибка среды выполнения VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="74c1d-118"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="74c1d-119">Произошла ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="74c1d-119">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="74c1d-120"><dt>**VFW \_ E — \_ неправильное \_ состояние**</dt></span><span class="sxs-lookup"><span data-stu-id="74c1d-120"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="74c1d-121">ПИН-код остановлен.</span><span class="sxs-lookup"><span data-stu-id="74c1d-121">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="74c1d-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74c1d-122">Remarks</span></span>

<span data-ttu-id="74c1d-123">Этот метод переопределяет метод [**кбасеинпутпин:: чеккстреаминг**](cbaseinputpin-checkstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="74c1d-123">This method overrides the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="74c1d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="74c1d-124">Requirements</span></span>



| <span data-ttu-id="74c1d-125">Требование</span><span class="sxs-lookup"><span data-stu-id="74c1d-125">Requirement</span></span> | <span data-ttu-id="74c1d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="74c1d-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74c1d-127">Header</span><span class="sxs-lookup"><span data-stu-id="74c1d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="74c1d-128"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74c1d-128"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="74c1d-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="74c1d-129">Library</span></span><br/> | <dl> <span data-ttu-id="74c1d-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="74c1d-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




