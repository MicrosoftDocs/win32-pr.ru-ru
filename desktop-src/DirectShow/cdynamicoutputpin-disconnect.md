---
description: Метод Disconnect прерывает текущее подключение ПИН-кода. Этот метод реализует метод Ипин::D соединения.
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: Метод Кдинамикаутпутпин. Disconnect (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65c61ecc825d703976aa3163be5922da1ac4471a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669142"
---
# <a name="cdynamicoutputpindisconnect-method"></a><span data-ttu-id="25fbb-104">Кдинамикаутпутпин. Disconnect, метод</span><span class="sxs-lookup"><span data-stu-id="25fbb-104">CDynamicOutputPin.Disconnect method</span></span>

<span data-ttu-id="25fbb-105">`Disconnect`Метод прерывает текущее подключение к ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="25fbb-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="25fbb-106">Этот метод реализует метод [**Ипин::D соединения**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="25fbb-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="25fbb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25fbb-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="25fbb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="25fbb-108">Parameters</span></span>

<span data-ttu-id="25fbb-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="25fbb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25fbb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25fbb-110">Return value</span></span>

<span data-ttu-id="25fbb-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="25fbb-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="25fbb-112">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="25fbb-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="25fbb-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="25fbb-113">Return code</span></span>                                                                             | <span data-ttu-id="25fbb-114">Описание</span><span class="sxs-lookup"><span data-stu-id="25fbb-114">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="25fbb-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="25fbb-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="25fbb-116">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="25fbb-116">The pin was not connected.</span></span><br/> |
| <dl> <span data-ttu-id="25fbb-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="25fbb-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="25fbb-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="25fbb-118">Success.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="25fbb-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25fbb-119">Remarks</span></span>

<span data-ttu-id="25fbb-120">Этот метод переопределяет метод [**кбасепин::D соединения**](cbasepin-disconnect.md) , чтобы разрешить отсоединение, пока фильтр активен.</span><span class="sxs-lookup"><span data-stu-id="25fbb-120">This method overrides the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method to enable disconnecting while the filter is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="25fbb-121">Требования</span><span class="sxs-lookup"><span data-stu-id="25fbb-121">Requirements</span></span>



| <span data-ttu-id="25fbb-122">Требование</span><span class="sxs-lookup"><span data-stu-id="25fbb-122">Requirement</span></span> | <span data-ttu-id="25fbb-123">Значение</span><span class="sxs-lookup"><span data-stu-id="25fbb-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25fbb-124">Header</span><span class="sxs-lookup"><span data-stu-id="25fbb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="25fbb-125"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25fbb-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="25fbb-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="25fbb-126">Library</span></span><br/> | <dl> <span data-ttu-id="25fbb-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="25fbb-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25fbb-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25fbb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25fbb-129">**Класс Кдинамикаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="25fbb-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




