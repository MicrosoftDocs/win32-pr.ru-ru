---
description: Метод Seek задает начальные и останавливаемые позиции потока.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: Метод Кпуллпин. Seek (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Seek
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f1a82ec549b5ceb888acc194a7abc2cd3eace47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669051"
---
# <a name="cpullpinseek-method"></a><span data-ttu-id="119d0-103">Кпуллпин. Seek, метод</span><span class="sxs-lookup"><span data-stu-id="119d0-103">CPullPin.Seek method</span></span>

<span data-ttu-id="119d0-104">`Seek`Метод задает начальные и останавливаемые позиции потока.</span><span class="sxs-lookup"><span data-stu-id="119d0-104">The `Seek` method sets the start and stop positions of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="119d0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="119d0-105">Syntax</span></span>


```C++
HRESULT Seek(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop
);
```



## <a name="parameters"></a><span data-ttu-id="119d0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="119d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="119d0-107">*тстарт*</span><span class="sxs-lookup"><span data-stu-id="119d0-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="119d0-108">Указывает начальную точку в байтах, умноженную на 10 000 000.</span><span class="sxs-lookup"><span data-stu-id="119d0-108">Specifies the start position, in bytes multiplied by 10,000,000.</span></span>

</dd> <dt>

<span data-ttu-id="119d0-109">*тстоп*</span><span class="sxs-lookup"><span data-stu-id="119d0-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="119d0-110">Указывает позиция окончания в байтах, умноженная на 10 000 000.</span><span class="sxs-lookup"><span data-stu-id="119d0-110">Specifies the stop position, in bytes multiplied by 10,000,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="119d0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="119d0-111">Return value</span></span>

<span data-ttu-id="119d0-112">Возвращает значение \_ ОК, если метод завершается успешно, или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="119d0-112">Returns S\_OK if the method succeeds, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="119d0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="119d0-113">Remarks</span></span>

<span data-ttu-id="119d0-114">Если рабочий поток запущен, метод приостанавливает поток, очищает граф фильтра и возобновляет поток.</span><span class="sxs-lookup"><span data-stu-id="119d0-114">If the worker thread is running, the method pauses the thread, flushes the filter graph, and resumes the thread.</span></span> <span data-ttu-id="119d0-115">Поток начинает извлечение данных из новой начальной должности.</span><span class="sxs-lookup"><span data-stu-id="119d0-115">The thread begins pulling data from the new start position.</span></span> <span data-ttu-id="119d0-116">В противном случае новые значения позиций вступают в силу при каждом запуске потока.</span><span class="sxs-lookup"><span data-stu-id="119d0-116">Otherwise, the new position values become effective whenever the thread is started.</span></span>

<span data-ttu-id="119d0-117">Позиции задаются относительно начала исходного источника.</span><span class="sxs-lookup"><span data-stu-id="119d0-117">Positions are relative to the start of the original source.</span></span> <span data-ttu-id="119d0-118">Умножьте требуемые смещения в байтах на константные единицы, которые определены в библиотеке базовых классов как 10 000 000.</span><span class="sxs-lookup"><span data-stu-id="119d0-118">Multiply the desired byte offsets by the constant UNITS, which is defined in the base class library as 10,000,000.</span></span>

<span data-ttu-id="119d0-119">Когда ПИН-код сначала соединяется, начальная и начальная позиции по умолчанию задаются в начале и в конце потока.</span><span class="sxs-lookup"><span data-stu-id="119d0-119">When the pin first connects, the stop and start positions default to the beginning and end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="119d0-120">Требования</span><span class="sxs-lookup"><span data-stu-id="119d0-120">Requirements</span></span>



| <span data-ttu-id="119d0-121">Требование</span><span class="sxs-lookup"><span data-stu-id="119d0-121">Requirement</span></span> | <span data-ttu-id="119d0-122">Значение</span><span class="sxs-lookup"><span data-stu-id="119d0-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="119d0-123">Header</span><span class="sxs-lookup"><span data-stu-id="119d0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="119d0-124"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="119d0-124"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="119d0-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="119d0-125">Library</span></span><br/> | <dl> <span data-ttu-id="119d0-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="119d0-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="119d0-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="119d0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="119d0-128">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="119d0-128">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




