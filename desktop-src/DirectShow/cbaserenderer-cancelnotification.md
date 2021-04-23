---
description: Метод Канцелнотификатион отменяет событие таймера, которое планирует подготовку к просмотру.
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: Кбасерендерер. Канцелнотификатион, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CancelNotification
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3330f369c5fcc45fe051a1964a504d5d40fcd091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668749"
---
# <a name="cbaserenderercancelnotification-method"></a><span data-ttu-id="5aae8-103">Кбасерендерер. Канцелнотификатион, метод</span><span class="sxs-lookup"><span data-stu-id="5aae8-103">CBaseRenderer.CancelNotification method</span></span>

<span data-ttu-id="5aae8-104">`CancelNotification`Метод отменяет событие таймера, которое планирует подготовку к просмотру.</span><span class="sxs-lookup"><span data-stu-id="5aae8-104">The `CancelNotification` method cancels the timer event that schedules rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aae8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5aae8-105">Syntax</span></span>


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a><span data-ttu-id="5aae8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5aae8-106">Parameters</span></span>

<span data-ttu-id="5aae8-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5aae8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5aae8-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5aae8-108">Return value</span></span>

<span data-ttu-id="5aae8-109">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5aae8-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="5aae8-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5aae8-110">Return code</span></span>                                                                             | <span data-ttu-id="5aae8-111">Описание</span><span class="sxs-lookup"><span data-stu-id="5aae8-111">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="5aae8-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="5aae8-112"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="5aae8-113">Нет ожидающего события таймера.</span><span class="sxs-lookup"><span data-stu-id="5aae8-113">There was no pending timer event.</span></span><br/> |
| <dl> <span data-ttu-id="5aae8-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5aae8-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="5aae8-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="5aae8-115">Success.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="5aae8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5aae8-116">Remarks</span></span>

<span data-ttu-id="5aae8-117">Фильтр вызывает этот метод при остановке потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="5aae8-117">The filter calls this method when streaming stops.</span></span> <span data-ttu-id="5aae8-118">Метод отменяет любую запланированную отрисовку.</span><span class="sxs-lookup"><span data-stu-id="5aae8-118">The method cancels any scheduled rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aae8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5aae8-119">Requirements</span></span>



| <span data-ttu-id="5aae8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5aae8-120">Requirement</span></span> | <span data-ttu-id="5aae8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5aae8-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aae8-122">Header</span><span class="sxs-lookup"><span data-stu-id="5aae8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5aae8-123"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5aae8-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5aae8-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5aae8-124">Library</span></span><br/> | <dl> <span data-ttu-id="5aae8-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5aae8-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aae8-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5aae8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aae8-127">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="5aae8-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




