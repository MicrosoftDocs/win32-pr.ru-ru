---
description: Метод Реаллокформатбуффер перераспределяет блок формата на новый размер.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: Кмедиатипе. Реаллокформатбуффер, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ReallocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22e861c61f01a7594d720833e2b3a4b923a1e183
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665299"
---
# <a name="cmediatypereallocformatbuffer-method"></a><span data-ttu-id="304d4-103">Кмедиатипе. Реаллокформатбуффер, метод</span><span class="sxs-lookup"><span data-stu-id="304d4-103">CMediaType.ReallocFormatBuffer method</span></span>

<span data-ttu-id="304d4-104">`ReallocFormatBuffer`Метод перераспределяет блок формата на новый размер.</span><span class="sxs-lookup"><span data-stu-id="304d4-104">The `ReallocFormatBuffer` method reallocates the format block to a new size.</span></span>

## <a name="syntax"></a><span data-ttu-id="304d4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="304d4-105">Syntax</span></span>


```C++
BYTE* ReallocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="304d4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="304d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="304d4-107">*length*</span><span class="sxs-lookup"><span data-stu-id="304d4-107">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="304d4-108">Новый размер, необходимый для блока формата в байтах.</span><span class="sxs-lookup"><span data-stu-id="304d4-108">New size required for the format block, in bytes.</span></span> <span data-ttu-id="304d4-109">Должен быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="304d4-109">Must be greater than zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="304d4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="304d4-110">Return value</span></span>

<span data-ttu-id="304d4-111">Возвращает указатель на новый блок в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="304d4-111">Returns a pointer to the new block if successful.</span></span> <span data-ttu-id="304d4-112">В противном случае возвращает либо указатель на старый блок формата, либо **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="304d4-112">Otherwise, returns either a pointer to the old format block, or **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="304d4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="304d4-113">Remarks</span></span>

<span data-ttu-id="304d4-114">Этот метод выделяет новый блок формата.</span><span class="sxs-lookup"><span data-stu-id="304d4-114">This method allocates a new format block.</span></span> <span data-ttu-id="304d4-115">В новый блок формата копируется как можно больше существующего блока формата.</span><span class="sxs-lookup"><span data-stu-id="304d4-115">It copies as much of the existing format block as possible into the new format block.</span></span> <span data-ttu-id="304d4-116">Если новый блок меньше существующего блока, существующий блок формата усекается.</span><span class="sxs-lookup"><span data-stu-id="304d4-116">If the new block is smaller than the existing block, the existing format block is truncated.</span></span> <span data-ttu-id="304d4-117">Если новый блок больше, содержимое дополнительного пространства не определено.</span><span class="sxs-lookup"><span data-stu-id="304d4-117">If the new block is larger, the contents of the additional space are undefined.</span></span> <span data-ttu-id="304d4-118">Для них явно не задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="304d4-118">They are not explicitly set to zero.</span></span>

<span data-ttu-id="304d4-119">Метод обновляет члены **кбформат** и **пбформат** структуры **\_ \_ типа мультимедиа AM** .</span><span class="sxs-lookup"><span data-stu-id="304d4-119">The method updates the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="304d4-120">Требования</span><span class="sxs-lookup"><span data-stu-id="304d4-120">Requirements</span></span>



| <span data-ttu-id="304d4-121">Требование</span><span class="sxs-lookup"><span data-stu-id="304d4-121">Requirement</span></span> | <span data-ttu-id="304d4-122">Значение</span><span class="sxs-lookup"><span data-stu-id="304d4-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="304d4-123">Header</span><span class="sxs-lookup"><span data-stu-id="304d4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="304d4-124"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="304d4-124"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="304d4-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="304d4-125">Library</span></span><br/> | <dl> <span data-ttu-id="304d4-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="304d4-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="304d4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="304d4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="304d4-128">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="304d4-128">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




