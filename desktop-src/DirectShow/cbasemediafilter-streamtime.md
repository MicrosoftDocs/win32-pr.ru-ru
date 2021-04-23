---
description: Метод Стреамтиме извлекает текущее время потока.
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
ms.openlocfilehash: 27ccc9c721c97742c09d043af4cca5d287747597
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656908"
---
# <a name="cbasemediafilterstreamtime-method"></a><span data-ttu-id="88a0b-103">Кбасемедиафилтер. Стреамтиме, метод</span><span class="sxs-lookup"><span data-stu-id="88a0b-103">CBaseMediaFilter.StreamTime method</span></span>

<span data-ttu-id="88a0b-104">`StreamTime`Метод получает текущее время потока.</span><span class="sxs-lookup"><span data-stu-id="88a0b-104">The `StreamTime` method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="88a0b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88a0b-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="88a0b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="88a0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88a0b-107">*ртстреам* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="88a0b-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="88a0b-108">Ссылка на объект [**крефтиме**](creftime.md) , который получает текущее время потока.</span><span class="sxs-lookup"><span data-stu-id="88a0b-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88a0b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88a0b-109">Return value</span></span>

<span data-ttu-id="88a0b-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88a0b-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="88a0b-111">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="88a0b-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="88a0b-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="88a0b-112">Return code</span></span>                                                                                      | <span data-ttu-id="88a0b-113">Описание</span><span class="sxs-lookup"><span data-stu-id="88a0b-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="88a0b-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="88a0b-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="88a0b-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="88a0b-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="88a0b-116"><dt>**VFW \_ E \_ без \_ часов**</dt></span><span class="sxs-lookup"><span data-stu-id="88a0b-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="88a0b-117">Нет доступных эталонных таймеров.</span><span class="sxs-lookup"><span data-stu-id="88a0b-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="88a0b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88a0b-118">Remarks</span></span>

<span data-ttu-id="88a0b-119">Время потока определяется как текущее время ссылки (в соответствии с заданным временем) минус время начала (заданное параметром [**кбасемедиафилтер:: m \_ тстарт**](cbasemediafilter-m-tstart.md)).</span><span class="sxs-lookup"><span data-stu-id="88a0b-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseMediaFilter::m\_tStart**](cbasemediafilter-m-tstart.md)).</span></span> <span data-ttu-id="88a0b-120">Метка времени в образце носителя указывает время потока, когда он должен быть визуализирован.</span><span class="sxs-lookup"><span data-stu-id="88a0b-120">A media sample's time stamp specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="88a0b-121">Если образец с отметкой времени, меньшим, чем текущее время потока, еще не был визуализирован, то это поздно.</span><span class="sxs-lookup"><span data-stu-id="88a0b-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

## <a name="requirements"></a><span data-ttu-id="88a0b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="88a0b-122">Requirements</span></span>



| <span data-ttu-id="88a0b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="88a0b-123">Requirement</span></span> | <span data-ttu-id="88a0b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="88a0b-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88a0b-125">Header</span><span class="sxs-lookup"><span data-stu-id="88a0b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="88a0b-126"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88a0b-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="88a0b-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="88a0b-127">Library</span></span><br/> | <dl> <span data-ttu-id="88a0b-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="88a0b-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88a0b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88a0b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88a0b-130">**Класс Кбасемедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="88a0b-130">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




