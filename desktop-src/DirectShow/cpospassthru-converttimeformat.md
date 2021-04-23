---
description: 'Метод Конверттимеформат преобразует из одного формата времени в другой. Этот метод реализует метод Имедиасикинг:: Конверттимеформат.'
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
ms.openlocfilehash: bcce3e24c46e3e59c6bad6b4fbd60b139806de73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675786"
---
# <a name="cpospassthruconverttimeformat-method"></a><span data-ttu-id="fba49-104">Кпоспасссру. Конверттимеформат, метод</span><span class="sxs-lookup"><span data-stu-id="fba49-104">CPosPassThru.ConvertTimeFormat method</span></span>

<span data-ttu-id="fba49-105">`ConvertTimeFormat`Метод преобразует из одного формата времени в другой.</span><span class="sxs-lookup"><span data-stu-id="fba49-105">The `ConvertTimeFormat` method converts from one time format to another.</span></span> <span data-ttu-id="fba49-106">Этот метод реализует метод [**имедиасикинг:: конверттимеформат**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .</span><span class="sxs-lookup"><span data-stu-id="fba49-106">This method implements the [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba49-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fba49-107">Syntax</span></span>


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a><span data-ttu-id="fba49-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fba49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba49-109">*птаржет*</span><span class="sxs-lookup"><span data-stu-id="fba49-109">*pTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="fba49-110">Указатель на переменную, которая получает преобразованное время.</span><span class="sxs-lookup"><span data-stu-id="fba49-110">Pointer to a variable that receives the converted time.</span></span>

</dd> <dt>

<span data-ttu-id="fba49-111">*птаржетформат*</span><span class="sxs-lookup"><span data-stu-id="fba49-111">*pTargetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="fba49-112">Указатель на идентификатор GUID формата времени целевого формата.</span><span class="sxs-lookup"><span data-stu-id="fba49-112">Pointer to the time format GUID of the target format.</span></span> <span data-ttu-id="fba49-113">Если **значение равно NULL**, используется текущий формат.</span><span class="sxs-lookup"><span data-stu-id="fba49-113">If **NULL**, the current format is used.</span></span>

</dd> <dt>

<span data-ttu-id="fba49-114">*Источник*</span><span class="sxs-lookup"><span data-stu-id="fba49-114">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="fba49-115">Значение времени, которое необходимо преобразовать.</span><span class="sxs-lookup"><span data-stu-id="fba49-115">Time value to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="fba49-116">*псаурцеформат*</span><span class="sxs-lookup"><span data-stu-id="fba49-116">*pSourceFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="fba49-117">Указатель на идентификатор GUID формата времени для преобразования.</span><span class="sxs-lookup"><span data-stu-id="fba49-117">Pointer to the time format GUID of the format to convert.</span></span> <span data-ttu-id="fba49-118">Если **значение равно NULL**, используется текущий формат.</span><span class="sxs-lookup"><span data-stu-id="fba49-118">If **NULL**, the current format is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fba49-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fba49-119">Return value</span></span>

<span data-ttu-id="fba49-120">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="fba49-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="fba49-121">Требования</span><span class="sxs-lookup"><span data-stu-id="fba49-121">Requirements</span></span>



| <span data-ttu-id="fba49-122">Требование</span><span class="sxs-lookup"><span data-stu-id="fba49-122">Requirement</span></span> | <span data-ttu-id="fba49-123">Значение</span><span class="sxs-lookup"><span data-stu-id="fba49-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fba49-124">Header</span><span class="sxs-lookup"><span data-stu-id="fba49-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fba49-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fba49-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fba49-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fba49-126">Library</span></span><br/> | <dl> <span data-ttu-id="fba49-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fba49-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fba49-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fba49-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba49-129">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="fba49-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="fba49-130">**Идентификаторы GUID формата времени**</span><span class="sxs-lookup"><span data-stu-id="fba49-130">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




