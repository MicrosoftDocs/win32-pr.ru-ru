---
description: 'Метод Stop останавливает объект. Этот метод реализует метод Имедиафилтер:: останавливаться.'
ms.assetid: 9282d90a-932c-4ba0-84f1-1de2c125bfbd
title: Метод Кбасемедиафилтер. останавливаться (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22bb45234c8be832f8ea30ed70b50c8f4919b7e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656923"
---
# <a name="cbasemediafilterstop-method"></a><span data-ttu-id="7094d-104">Кбасемедиафилтер. останавливаться, метод</span><span class="sxs-lookup"><span data-stu-id="7094d-104">CBaseMediaFilter.Stop method</span></span>

<span data-ttu-id="7094d-105">`Stop`Метод останавливает объект.</span><span class="sxs-lookup"><span data-stu-id="7094d-105">The `Stop` method stops the object.</span></span> <span data-ttu-id="7094d-106">Этот метод реализует метод [**имедиафилтер:: останавливаться**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="7094d-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7094d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7094d-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="7094d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7094d-108">Parameters</span></span>

<span data-ttu-id="7094d-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7094d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7094d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7094d-110">Return value</span></span>

<span data-ttu-id="7094d-111">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7094d-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7094d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7094d-112">Remarks</span></span>

<span data-ttu-id="7094d-113">В базовом классе этот метод устанавливает переменную члена [**\_ состояния кбасемедиафилтер:: m**](cbasemediafilter-m-state.md) в состояние \_ Stopped, но не выполняет никаких других действий.</span><span class="sxs-lookup"><span data-stu-id="7094d-113">In the base class, this method sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Stopped but does nothing else.</span></span>

## <a name="requirements"></a><span data-ttu-id="7094d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7094d-114">Requirements</span></span>



| <span data-ttu-id="7094d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7094d-115">Requirement</span></span> | <span data-ttu-id="7094d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7094d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7094d-117">Header</span><span class="sxs-lookup"><span data-stu-id="7094d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7094d-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7094d-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7094d-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7094d-119">Library</span></span><br/> | <dl> <span data-ttu-id="7094d-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7094d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7094d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7094d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7094d-122">**Класс Кбасемедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="7094d-122">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




