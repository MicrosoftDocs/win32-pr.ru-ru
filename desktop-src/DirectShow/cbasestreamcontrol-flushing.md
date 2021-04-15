---
description: Метод очистки уведомляет базовый класс о том, что ПИН-код начал или прекратил запись на диск.
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: Метод Кбасестреамконтрол. Flush (Стрмктл. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.Flushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d4a3a2375ca799f5dd35def03295f29f61c0583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668953"
---
# <a name="cbasestreamcontrolflushing-method"></a><span data-ttu-id="01bbd-103">Метод Кбасестреамконтрол. Flush</span><span class="sxs-lookup"><span data-stu-id="01bbd-103">CBaseStreamControl.Flushing method</span></span>

<span data-ttu-id="01bbd-104">`Flushing`Метод уведомляет базовый класс о том, что ПИН-код запущен или прекратил запись на диск.</span><span class="sxs-lookup"><span data-stu-id="01bbd-104">The `Flushing` method notifies the base class that the pin has started or stopped flushing.</span></span>

## <a name="syntax"></a><span data-ttu-id="01bbd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01bbd-105">Syntax</span></span>


```C++
void Flushing(
   BOOL bInProgress
);
```



## <a name="parameters"></a><span data-ttu-id="01bbd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="01bbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01bbd-107">*бинпрогресс*</span><span class="sxs-lookup"><span data-stu-id="01bbd-107">*bInProgress*</span></span> 
</dt> <dd>

<span data-ttu-id="01bbd-108">Задает логическое значение, указывающее, является ли ПИН-код записью на диск.</span><span class="sxs-lookup"><span data-stu-id="01bbd-108">Specifies a Boolean value that indicates whether the pin is flushing.</span></span> <span data-ttu-id="01bbd-109">Используйте значение **true** , когда ПИН-код начинает операцию записи на диск, и **значение false** , если ПИН-код завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="01bbd-109">Use the value **TRUE** when the pin begins a flush operation, and **FALSE** when the pin ends a flush operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01bbd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01bbd-110">Return value</span></span>

<span data-ttu-id="01bbd-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="01bbd-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01bbd-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01bbd-112">Remarks</span></span>

<span data-ttu-id="01bbd-113">ПИН-код должен вызывать этот метод из методов [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) и [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="01bbd-113">The pin must call this method from within its [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods.</span></span> <span data-ttu-id="01bbd-114">Укажите **true** в **бегинфлуш** и **false** в **ендфлуш**.</span><span class="sxs-lookup"><span data-stu-id="01bbd-114">Specify **TRUE** in **BeginFlush** and **FALSE** in **EndFlush**.</span></span>

<span data-ttu-id="01bbd-115">Этот метод заставляет метод [**кбасестреамконтрол:: чеккстреамстате**](cbasestreamcontrol-checkstreamstate.md) прерывать ожидание.</span><span class="sxs-lookup"><span data-stu-id="01bbd-115">This method causes the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method to stop waiting.</span></span> <span data-ttu-id="01bbd-116">Пока ПИН-код очищается, **чеккстреамстате** всегда возвращает ПОТОКовую \_ отмену.</span><span class="sxs-lookup"><span data-stu-id="01bbd-116">While the pin is flushing, **CheckStreamState** always returns STREAM\_DISCARDING.</span></span>

## <a name="requirements"></a><span data-ttu-id="01bbd-117">Требования</span><span class="sxs-lookup"><span data-stu-id="01bbd-117">Requirements</span></span>



| <span data-ttu-id="01bbd-118">Требование</span><span class="sxs-lookup"><span data-stu-id="01bbd-118">Requirement</span></span> | <span data-ttu-id="01bbd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="01bbd-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01bbd-120">Header</span><span class="sxs-lookup"><span data-stu-id="01bbd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="01bbd-121"><dt>Стрмктл. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01bbd-121"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="01bbd-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="01bbd-122">Library</span></span><br/> | <dl> <span data-ttu-id="01bbd-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="01bbd-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01bbd-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01bbd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01bbd-125">**Класс Кбасестреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="01bbd-125">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




