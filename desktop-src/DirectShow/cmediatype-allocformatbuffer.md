---
description: Метод Аллокформатбуффер выделяет память для блока Format.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: Кмедиатипе. Аллокформатбуффер, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.AllocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6a9314fd06734adcc367b7be34dc8d6d1b9d996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665061"
---
# <a name="cmediatypeallocformatbuffer-method"></a><span data-ttu-id="2c459-103">Кмедиатипе. Аллокформатбуффер, метод</span><span class="sxs-lookup"><span data-stu-id="2c459-103">CMediaType.AllocFormatBuffer method</span></span>

<span data-ttu-id="2c459-104">`AllocFormatBuffer`Метод выделяет память для блока Format.</span><span class="sxs-lookup"><span data-stu-id="2c459-104">The `AllocFormatBuffer` method allocates memory for the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c459-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c459-105">Syntax</span></span>


```C++
BYTE* AllocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="2c459-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c459-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c459-107">*length*</span><span class="sxs-lookup"><span data-stu-id="2c459-107">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="2c459-108">Требуемый размер блока формата в байтах.</span><span class="sxs-lookup"><span data-stu-id="2c459-108">Size required for the format block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c459-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c459-109">Return value</span></span>

<span data-ttu-id="2c459-110">Возвращает указатель на новый блок в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="2c459-110">Returns a pointer to the new block if successful.</span></span> <span data-ttu-id="2c459-111">В противном случае возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2c459-111">Otherwise, returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c459-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c459-112">Remarks</span></span>

<span data-ttu-id="2c459-113">Если метод успешно выделяет новый блок формата, он освобождает существующий блок формата.</span><span class="sxs-lookup"><span data-stu-id="2c459-113">If the method successfully allocates a new format block, it frees the existing format block.</span></span> <span data-ttu-id="2c459-114">Если выделение завершается неудачей, метод оставляет существующий блок формата.</span><span class="sxs-lookup"><span data-stu-id="2c459-114">If the allocation fails, the method leaves the existing format block.</span></span>

<span data-ttu-id="2c459-115">Метод обновляет члены **кбформат** и **пбформат** структуры **\_ \_ типа мультимедиа AM** .</span><span class="sxs-lookup"><span data-stu-id="2c459-115">The method updates the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c459-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2c459-116">Requirements</span></span>



| <span data-ttu-id="2c459-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2c459-117">Requirement</span></span> | <span data-ttu-id="2c459-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2c459-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c459-119">Header</span><span class="sxs-lookup"><span data-stu-id="2c459-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2c459-120"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c459-120"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="2c459-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2c459-121">Library</span></span><br/> | <dl> <span data-ttu-id="2c459-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="2c459-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c459-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c459-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c459-124">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="2c459-124">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




