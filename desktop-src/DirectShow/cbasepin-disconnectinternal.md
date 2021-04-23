---
description: Метод Дисконнектинтернал прерывает текущее подключение ПИН-кода.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: Кбасепин. Дисконнектинтернал, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisconnectInternal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0891a9446e09c56e3845c02217d39037aad38bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657515"
---
# <a name="cbasepindisconnectinternal-method"></a><span data-ttu-id="9757e-103">Кбасепин. Дисконнектинтернал, метод</span><span class="sxs-lookup"><span data-stu-id="9757e-103">CBasePin.DisconnectInternal method</span></span>

<span data-ttu-id="9757e-104">`DisconnectInternal`Метод прерывает текущее подключение к ПИН-коду.</span><span class="sxs-lookup"><span data-stu-id="9757e-104">The `DisconnectInternal` method breaks the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9757e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9757e-105">Syntax</span></span>


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a><span data-ttu-id="9757e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9757e-106">Parameters</span></span>

<span data-ttu-id="9757e-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9757e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9757e-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9757e-108">Return value</span></span>

<span data-ttu-id="9757e-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9757e-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9757e-110">Возможные значения перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9757e-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="9757e-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9757e-111">Return code</span></span>                                                                                         | <span data-ttu-id="9757e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9757e-112">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9757e-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9757e-113"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="9757e-114">ПИН-код не подключен.</span><span class="sxs-lookup"><span data-stu-id="9757e-114">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="9757e-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9757e-115"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="9757e-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="9757e-116">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="9757e-117"><dt>**VFW \_ E \_ не \_ остановлен**</dt></span><span class="sxs-lookup"><span data-stu-id="9757e-117"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="9757e-118">Фильтр активен, и ПИН-код не поддерживает динамическое повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="9757e-118">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9757e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9757e-119">Remarks</span></span>

<span data-ttu-id="9757e-120">Метод [**кбасепин::D метода соединения**](cbasepin-disconnect.md) делегирует процесс отключения этому методу.</span><span class="sxs-lookup"><span data-stu-id="9757e-120">The [**CBasePin::Disconnect**](cbasepin-disconnect.md) method delegates the disconnect process to this method.</span></span> <span data-ttu-id="9757e-121">Этот метод вызывает метод [**кбасепин:: бреакконнект**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="9757e-121">This method calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="9757e-122">Он также освобождает счетчик ссылок на другой ПИН-код, который удерживается переменной члена, [**\_ подключенной к кбасепин:: m**](cbasepin-m-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="9757e-122">It also releases the reference count on the other pin, which is held by the [**CBasePin::m\_Connected**](cbasepin-m-connected.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="9757e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9757e-123">Requirements</span></span>



| <span data-ttu-id="9757e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9757e-124">Requirement</span></span> | <span data-ttu-id="9757e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9757e-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9757e-126">Header</span><span class="sxs-lookup"><span data-stu-id="9757e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9757e-127"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9757e-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9757e-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9757e-128">Library</span></span><br/> | <dl> <span data-ttu-id="9757e-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9757e-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9757e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9757e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9757e-131">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="9757e-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




