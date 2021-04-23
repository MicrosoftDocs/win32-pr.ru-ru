---
description: 'Метод Сетпоситионс задает текущую и заданную позиции. Этот метод реализует метод Имедиасикинг:: Сетпоситионс.'
ms.assetid: 4359fe1f-f922-4a4d-beaa-8e13c72f407c
title: Ксаурцесикинг. Сетпоситионс, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 342ca7d85fe9358b914709b7887216b62e03521d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657362"
---
# <a name="csourceseekingsetpositions-method"></a><span data-ttu-id="2b08f-104">Ксаурцесикинг. Сетпоситионс, метод</span><span class="sxs-lookup"><span data-stu-id="2b08f-104">CSourceSeeking.SetPositions method</span></span>

<span data-ttu-id="2b08f-105">`SetPositions`Метод задает текущее расположение и точку окончания.</span><span class="sxs-lookup"><span data-stu-id="2b08f-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="2b08f-106">Этот метод реализует метод [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="2b08f-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b08f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b08f-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    CurrentFlags,
   LONGLONG *pStop,
   DWORD    StopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2b08f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b08f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b08f-109">*пкуррент*</span><span class="sxs-lookup"><span data-stu-id="2b08f-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="2b08f-110">Указатель на переменную, которая указывает текущую позиции.</span><span class="sxs-lookup"><span data-stu-id="2b08f-110">Pointer to a variable that specifies the current position.</span></span>

</dd> <dt>

<span data-ttu-id="2b08f-111">*куррентфлагс*</span><span class="sxs-lookup"><span data-stu-id="2b08f-111">*CurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="2b08f-112">Побитовое сочетание флагов.</span><span class="sxs-lookup"><span data-stu-id="2b08f-112">Bitwise combination of flags.</span></span> <span data-ttu-id="2b08f-113">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="2b08f-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2b08f-114">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="2b08f-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="2b08f-115">Указатель на переменную, задающую время окончания в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="2b08f-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="2b08f-116">*стопфлагс*</span><span class="sxs-lookup"><span data-stu-id="2b08f-116">*StopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="2b08f-117">Побитовое сочетание флагов.</span><span class="sxs-lookup"><span data-stu-id="2b08f-117">Bitwise combination of flags.</span></span> <span data-ttu-id="2b08f-118">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="2b08f-118">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b08f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b08f-119">Return value</span></span>

<span data-ttu-id="2b08f-120">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2b08f-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2b08f-121">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2b08f-121">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="2b08f-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2b08f-122">Return code</span></span>                                                                                  | <span data-ttu-id="2b08f-123">Описание</span><span class="sxs-lookup"><span data-stu-id="2b08f-123">Description</span></span>                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="2b08f-124"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2b08f-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2b08f-125">Успешно</span><span class="sxs-lookup"><span data-stu-id="2b08f-125">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="2b08f-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2b08f-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2b08f-127">Недопустимые флаги</span><span class="sxs-lookup"><span data-stu-id="2b08f-127">Invalid flags</span></span><br/>             |
| <dl> <span data-ttu-id="2b08f-128"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="2b08f-128"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="2b08f-129">**Пустой** аргумент указателя</span><span class="sxs-lookup"><span data-stu-id="2b08f-129">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2b08f-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b08f-130">Remarks</span></span>

<span data-ttu-id="2b08f-131">Поддерживаются следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="2b08f-131">The following flags are supported:</span></span>

-   <span data-ttu-id="2b08f-132">\_Поиск в \_ позиционировании</span><span class="sxs-lookup"><span data-stu-id="2b08f-132">AM\_SEEKING\_NoPositioning</span></span>
-   <span data-ttu-id="2b08f-133">\_Поиск \_ абсолутепоситионинг</span><span class="sxs-lookup"><span data-stu-id="2b08f-133">AM\_SEEKING\_AbsolutePositioning</span></span>
-   <span data-ttu-id="2b08f-134">\_Поиск \_ релативепоситионинг</span><span class="sxs-lookup"><span data-stu-id="2b08f-134">AM\_SEEKING\_RelativePositioning</span></span>
-   <span data-ttu-id="2b08f-135">\_Поиск \_ инкременталпоситионинг (только *пстоп* )</span><span class="sxs-lookup"><span data-stu-id="2b08f-135">AM\_SEEKING\_IncrementalPositioning (*pStop* only)</span></span>

<span data-ttu-id="2b08f-136">Дополнительные сведения см. в разделе [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="2b08f-136">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

<span data-ttu-id="2b08f-137">Этот метод обновляет значения переменных членов [**ксаурцесикинг:: m \_ Ртстарт**](csourceseeking-m-rtstart.md) и [**ксаурцесикинг:: m \_ ртстоп**](csourceseeking-m-rtstop.md) , а затем вызывает чистые виртуальные методы [**ксаурцесикинг:: чанжестарт**](csourceseeking-changestart.md) и [**ксаурцесикинг:: ChangeStop**](csourceseeking-changestop.md).</span><span class="sxs-lookup"><span data-stu-id="2b08f-137">This method updates the values of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) and [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variables, and then calls the pure virtual methods [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b08f-138">Требования</span><span class="sxs-lookup"><span data-stu-id="2b08f-138">Requirements</span></span>



| <span data-ttu-id="2b08f-139">Требование</span><span class="sxs-lookup"><span data-stu-id="2b08f-139">Requirement</span></span> | <span data-ttu-id="2b08f-140">Значение</span><span class="sxs-lookup"><span data-stu-id="2b08f-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b08f-141">Header</span><span class="sxs-lookup"><span data-stu-id="2b08f-141">Header</span></span><br/>  | <dl> <span data-ttu-id="2b08f-142"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b08f-142"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2b08f-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2b08f-143">Library</span></span><br/> | <dl> <span data-ttu-id="2b08f-144"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2b08f-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b08f-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b08f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b08f-146">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="2b08f-146">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




