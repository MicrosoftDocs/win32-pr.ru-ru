---
description: 'Кпоспасссру. Конверттимеформат, метод Конверттимеформат преобразует из одного формата времени в другой. Этот метод реализует метод Имедиасикинг:: Конверттимеформат.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Кпоспасссру. Конверттимеформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc463cb6dc891e677266289971a1dac8b335a8c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098962"
---
# <a name="cpospassthruconverttimeformat-method"></a><span data-ttu-id="6b6fc-104">Кпоспасссру. Конверттимеформат, метод</span><span class="sxs-lookup"><span data-stu-id="6b6fc-104">CPosPassThru.ConvertTimeFormat method</span></span>

<span data-ttu-id="6b6fc-105">`ConvertTimeFormat`Метод преобразует из одного формата времени в другой.</span><span class="sxs-lookup"><span data-stu-id="6b6fc-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="6b6fc-106">Этот метод реализует метод [**имедиасикинг:: конверттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .</span><span class="sxs-lookup"><span data-stu-id="6b6fc-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b6fc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b6fc-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="6b6fc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b6fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b6fc-109">*птаржет*</span><span class="sxs-lookup"><span data-stu-id="6b6fc-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="6b6fc-110">Указатель на переменную, которая получает преобразованное время.</span><span class="sxs-lookup"><span data-stu-id="6b6fc-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="6b6fc-111">*птаржетформат*</span><span class="sxs-lookup"><span data-stu-id="6b6fc-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="6b6fc-112">Указатель на идентификатор GUID формата времени целевого формата.</span><span class="sxs-lookup"><span data-stu-id="6b6fc-112">Pointer to the time format GUID of the target format.</span></span> <span data-ttu-id="6b6fc-113">Если **значение равно NULL**, используется текущий формат.</span><span class="sxs-lookup"><span data-stu-id="6b6fc-113">If **NULL**, the current format is used.</span></span>

</dd> <dt>

<span data-ttu-id="6b6fc-114">*Источник*</span><span class="sxs-lookup"><span data-stu-id="6b6fc-114">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="6b6fc-115">Значение времени, которое необходимо преобразовать.</span><span class="sxs-lookup"><span data-stu-id="6b6fc-115">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="6b6fc-116">*псаурцеформат*</span><span class="sxs-lookup"><span data-stu-id="6b6fc-116">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="6b6fc-117">Указатель на идентификатор GUID формата времени для преобразования.</span><span class="sxs-lookup"><span data-stu-id="6b6fc-117">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="6b6fc-118">Если **значение равно NULL**, используется текущий формат.</span><span class="sxs-lookup"><span data-stu-id="6b6fc-118">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b6fc-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b6fc-119">Return value</span></span>

<span data-ttu-id="6b6fc-120">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="6b6fc-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b6fc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="6b6fc-121">Requirements</span></span>



| <span data-ttu-id="6b6fc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="6b6fc-122">Requirement</span></span> | <span data-ttu-id="6b6fc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6b6fc-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b6fc-124">Header</span><span class="sxs-lookup"><span data-stu-id="6b6fc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6b6fc-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b6fc-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6b6fc-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6b6fc-126">Library</span></span><br/> | <dl> <span data-ttu-id="6b6fc-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6b6fc-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b6fc-128">См. также</span><span class="sxs-lookup"><span data-stu-id="6b6fc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b6fc-129">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="6b6fc-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="6b6fc-130">**Идентификаторы GUID формата времени**</span><span class="sxs-lookup"><span data-stu-id="6b6fc-130">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




