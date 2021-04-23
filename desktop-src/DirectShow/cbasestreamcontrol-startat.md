---
description: 'Метод StartAt информирует ПИН-код о начале доставки данных. Этот метод реализует метод Иамстреамконтрол:: StartAt.'
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: Метод Кбасестреамконтрол. StartAt (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7adcf7cbd435992333bb8ae59d5ab1674056223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656835"
---
# <a name="cbasestreamcontrolstartat-method"></a><span data-ttu-id="6b0ae-104">Кбасестреамконтрол. StartAt, метод</span><span class="sxs-lookup"><span data-stu-id="6b0ae-104">CBaseStreamControl.StartAt method</span></span>

<span data-ttu-id="6b0ae-105">`StartAt`Метод информирует ПИН-код, когда следует начать доставку данных.</span><span class="sxs-lookup"><span data-stu-id="6b0ae-105">The `StartAt` method informs the pin when to start delivering data.</span></span> <span data-ttu-id="6b0ae-106">Этот метод реализует метод [**иамстреамконтрол:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="6b0ae-106">This method implements the [**IAMStreamControl::StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b0ae-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b0ae-107">Syntax</span></span>


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a><span data-ttu-id="6b0ae-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b0ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b0ae-109">*птстарт*</span><span class="sxs-lookup"><span data-stu-id="6b0ae-109">*ptStart*</span></span> 
</dt> <dd>

<span data-ttu-id="6b0ae-110">Указатель на значение [**\_ времени ссылки**](reference-time.md) , указывающее, когда ПИН-код должен начать доставку данных.</span><span class="sxs-lookup"><span data-stu-id="6b0ae-110">Pointer to a [**REFERENCE\_TIME**](reference-time.md) value that specifies when the pin should start delivering data.</span></span>

</dd> <dt>

<span data-ttu-id="6b0ae-111">*двкукие*</span><span class="sxs-lookup"><span data-stu-id="6b0ae-111">*dwCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="6b0ae-112">Указывает значение для отправки вместе с уведомлением о запуске.</span><span class="sxs-lookup"><span data-stu-id="6b0ae-112">Specifies a value to send along with the start notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b0ae-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b0ae-113">Return value</span></span>

<span data-ttu-id="6b0ae-114">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6b0ae-114">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b0ae-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6b0ae-115">Requirements</span></span>



| <span data-ttu-id="6b0ae-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6b0ae-116">Requirement</span></span> | <span data-ttu-id="6b0ae-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6b0ae-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b0ae-118">Header</span><span class="sxs-lookup"><span data-stu-id="6b0ae-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6b0ae-119"><dt>Стрмктл. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b0ae-119"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6b0ae-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6b0ae-120">Library</span></span><br/> | <dl> <span data-ttu-id="6b0ae-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6b0ae-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b0ae-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b0ae-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b0ae-123">**Класс Кбасестреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="6b0ae-123">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




