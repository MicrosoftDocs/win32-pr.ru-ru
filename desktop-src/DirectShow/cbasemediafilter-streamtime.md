---
description: Кбасемедиафилтер. Стреамтиме, метод Стреамтиме извлекает текущее время потока.
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: Кбасемедиафилтер. Стреамтиме, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a90bb7d97825c14f11c75dd42d696fa302f8e3d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096252"
---
# <a name="cbasemediafilterstreamtime-method"></a><span data-ttu-id="0caca-103">Кбасемедиафилтер. Стреамтиме, метод</span><span class="sxs-lookup"><span data-stu-id="0caca-103">CBaseMediaFilter.StreamTime method</span></span>

<span data-ttu-id="0caca-104">`StreamTime`Метод получает текущее время потока.</span><span class="sxs-lookup"><span data-stu-id="0caca-104">The `StreamTime` method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="0caca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0caca-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="0caca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0caca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0caca-107">*ртстреам* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="0caca-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="0caca-108">Ссылка на объект [**крефтиме**](creftime.md) , который получает текущее время потока.</span><span class="sxs-lookup"><span data-stu-id="0caca-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0caca-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0caca-109">Return value</span></span>

<span data-ttu-id="0caca-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0caca-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0caca-111">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0caca-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="0caca-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0caca-112">Return code</span></span>                                                                                      | <span data-ttu-id="0caca-113">Описание</span><span class="sxs-lookup"><span data-stu-id="0caca-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="0caca-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0caca-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="0caca-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="0caca-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="0caca-116"><dt>**VFW \_ E \_ без \_ часов**</dt></span><span class="sxs-lookup"><span data-stu-id="0caca-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="0caca-117">Нет доступных эталонных таймеров.</span><span class="sxs-lookup"><span data-stu-id="0caca-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0caca-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="0caca-118">Remarks</span></span>

<span data-ttu-id="0caca-119">Время потока определяется как текущее время ссылки (в соответствии с заданным временем) минус время начала (заданное параметром [**кбасемедиафилтер:: m \_ тстарт**](cbasemediafilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="0caca-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseMediaFilter::m\_tStart**](cbasemediafilter-m-tstart.md)).</span></span> <span data-ttu-id="0caca-120">Метка времени в образце носителя указывает время потока, когда он должен быть визуализирован.</span><span class="sxs-lookup"><span data-stu-id="0caca-120">A media sample's time stamp specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="0caca-121">Если образец с отметкой времени, меньшим, чем текущее время потока, еще не был визуализирован, то это поздно.</span><span class="sxs-lookup"><span data-stu-id="0caca-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

## <a name="requirements"></a><span data-ttu-id="0caca-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0caca-122">Requirements</span></span>



| <span data-ttu-id="0caca-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0caca-123">Requirement</span></span> | <span data-ttu-id="0caca-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0caca-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0caca-125">Header</span><span class="sxs-lookup"><span data-stu-id="0caca-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0caca-126"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0caca-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0caca-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0caca-127">Library</span></span><br/> | <dl> <span data-ttu-id="0caca-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0caca-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0caca-129">См. также</span><span class="sxs-lookup"><span data-stu-id="0caca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0caca-130">**Класс Кбасемедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="0caca-130">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




