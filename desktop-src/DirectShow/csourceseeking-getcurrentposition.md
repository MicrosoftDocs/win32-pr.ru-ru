---
description: Метод Жеткуррентпоситион извлекает текущую точку относительно общей продолжительности потока. Не реализован.
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: Ксаурцесикинг. Жеткуррентпоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52f99323e5ce3a62f1964cad2586a18ad473cdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657506"
---
# <a name="csourceseekinggetcurrentposition-method"></a><span data-ttu-id="23e89-104">Ксаурцесикинг. Жеткуррентпоситион, метод</span><span class="sxs-lookup"><span data-stu-id="23e89-104">CSourceSeeking.GetCurrentPosition method</span></span>

<span data-ttu-id="23e89-105">`GetCurrentPosition`Метод получает текущую координату относительно общей продолжительности потока.</span><span class="sxs-lookup"><span data-stu-id="23e89-105">The `GetCurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="23e89-106">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="23e89-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="23e89-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23e89-107">Syntax</span></span>


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a><span data-ttu-id="23e89-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="23e89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23e89-109">*пкуррент*</span><span class="sxs-lookup"><span data-stu-id="23e89-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="23e89-110">Указатель на переменную, которая получает текущую координату в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="23e89-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23e89-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23e89-111">Return value</span></span>

<span data-ttu-id="23e89-112">Возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="23e89-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="23e89-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23e89-113">Remarks</span></span>

<span data-ttu-id="23e89-114">Фильтры источников обычно не поддерживают этот метод.</span><span class="sxs-lookup"><span data-stu-id="23e89-114">Source filters typically do not support this method.</span></span> <span data-ttu-id="23e89-115">Вместо этого фильтры модуля подготовки отчетов сообщают о текущей позицией через класс [**крендерерпоспасссру**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="23e89-115">Instead, renderer filters report the current position through the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="23e89-116">Требования</span><span class="sxs-lookup"><span data-stu-id="23e89-116">Requirements</span></span>



| <span data-ttu-id="23e89-117">Требование</span><span class="sxs-lookup"><span data-stu-id="23e89-117">Requirement</span></span> | <span data-ttu-id="23e89-118">Значение</span><span class="sxs-lookup"><span data-stu-id="23e89-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23e89-119">Header</span><span class="sxs-lookup"><span data-stu-id="23e89-119">Header</span></span><br/>  | <dl> <span data-ttu-id="23e89-120"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23e89-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="23e89-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="23e89-121">Library</span></span><br/> | <dl> <span data-ttu-id="23e89-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="23e89-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23e89-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23e89-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e89-124">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="23e89-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




