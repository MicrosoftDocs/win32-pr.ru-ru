---
description: Метод Pause приостанавливает фильтр. Этот метод реализует метод Имедиафилтер::P Аусе.
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: Метод Кбасефилтер. Pause (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a90e78084f2320d0df7da806b6138571c9a5bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657890"
---
# <a name="cbasefilterpause-method"></a><span data-ttu-id="4a58e-104">Кбасефилтер. Pause, метод</span><span class="sxs-lookup"><span data-stu-id="4a58e-104">CBaseFilter.Pause method</span></span>

<span data-ttu-id="4a58e-105">`Pause`Метод приостанавливает фильтр.</span><span class="sxs-lookup"><span data-stu-id="4a58e-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="4a58e-106">Этот метод реализует метод [**имедиафилтер::P Аусе**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="4a58e-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a58e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a58e-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="4a58e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a58e-108">Parameters</span></span>

<span data-ttu-id="4a58e-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4a58e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a58e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a58e-110">Return value</span></span>

<span data-ttu-id="4a58e-111">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="4a58e-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a58e-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a58e-112">Remarks</span></span>

<span data-ttu-id="4a58e-113">Этот метод вызывает метод [**кбасепин:: Active**](cbasepin-active.md) для каждого подключенного контакта фильтра.</span><span class="sxs-lookup"><span data-stu-id="4a58e-113">This method calls the [**CBasePin::Active**](cbasepin-active.md) method on each of the filter's connected pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a58e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4a58e-114">Requirements</span></span>



| <span data-ttu-id="4a58e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4a58e-115">Requirement</span></span> | <span data-ttu-id="4a58e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4a58e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a58e-117">Header</span><span class="sxs-lookup"><span data-stu-id="4a58e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4a58e-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a58e-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4a58e-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4a58e-119">Library</span></span><br/> | <dl> <span data-ttu-id="4a58e-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4a58e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a58e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a58e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a58e-122">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="4a58e-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




