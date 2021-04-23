---
description: Метод Disconnect прерывает текущее подключение ПИН-кода. Этот метод реализует метод Ипин::D соединения.
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: Метод Кбасепин. Disconnect (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98cbf894767eeb89042134344df218f2c18bc1be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668775"
---
# <a name="cbasepindisconnect-method"></a><span data-ttu-id="1e98a-104">Кбасепин. Disconnect, метод</span><span class="sxs-lookup"><span data-stu-id="1e98a-104">CBasePin.Disconnect method</span></span>

<span data-ttu-id="1e98a-105">`Disconnect`Метод прерывает текущее подключение к ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="1e98a-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="1e98a-106">Этот метод реализует метод [**Ипин::D соединения**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="1e98a-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e98a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e98a-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="1e98a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e98a-108">Parameters</span></span>

<span data-ttu-id="1e98a-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1e98a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e98a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e98a-110">Return value</span></span>

<span data-ttu-id="1e98a-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e98a-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1e98a-112">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1e98a-112">Possible values include those in the following table.</span></span>



| <span data-ttu-id="1e98a-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1e98a-113">Return code</span></span>                                                                                         | <span data-ttu-id="1e98a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="1e98a-114">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e98a-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1e98a-115"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="1e98a-116">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="1e98a-116">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="1e98a-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1e98a-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="1e98a-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="1e98a-118">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="1e98a-119"><dt>**VFW \_ E \_ не \_ остановлен**</dt></span><span class="sxs-lookup"><span data-stu-id="1e98a-119"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="1e98a-120">Фильтр активен, и ПИН-код не поддерживает динамическое повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="1e98a-120">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1e98a-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e98a-121">Remarks</span></span>

<span data-ttu-id="1e98a-122">Базовый класс делегирует большую часть работы методу [**кбасепин::D исконнектинтернал**](cbasepin-disconnectinternal.md) .</span><span class="sxs-lookup"><span data-stu-id="1e98a-122">The base class delegates most of the work to the [**CBasePin::DisconnectInternal**](cbasepin-disconnectinternal.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e98a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1e98a-123">Requirements</span></span>



| <span data-ttu-id="1e98a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1e98a-124">Requirement</span></span> | <span data-ttu-id="1e98a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1e98a-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e98a-126">Header</span><span class="sxs-lookup"><span data-stu-id="1e98a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1e98a-127"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e98a-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1e98a-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1e98a-128">Library</span></span><br/> | <dl> <span data-ttu-id="1e98a-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1e98a-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e98a-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e98a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e98a-131">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="1e98a-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




