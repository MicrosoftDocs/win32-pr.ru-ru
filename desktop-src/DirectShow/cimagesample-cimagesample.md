---
description: Метод конструктора.
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Конструктор Цимажесампле. Цимажесампле (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805be59cfc899b6461fa8c761eebb5821118640f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665230"
---
# <a name="cimagesamplecimagesample-constructor"></a><span data-ttu-id="db6ba-103">Цимажесампле. Цимажесампле, конструктор</span><span class="sxs-lookup"><span data-stu-id="db6ba-103">CImageSample.CImageSample constructor</span></span>

<span data-ttu-id="db6ba-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="db6ba-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="db6ba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db6ba-105">Syntax</span></span>


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a><span data-ttu-id="db6ba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db6ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db6ba-107">*паллокатор*</span><span class="sxs-lookup"><span data-stu-id="db6ba-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="db6ba-108">Указатель на распределитель, создавший этот образец.</span><span class="sxs-lookup"><span data-stu-id="db6ba-108">Pointer to the allocator that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="db6ba-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="db6ba-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="db6ba-110">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="db6ba-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="db6ba-111">*фр*</span><span class="sxs-lookup"><span data-stu-id="db6ba-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="db6ba-112">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="db6ba-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="db6ba-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="db6ba-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="db6ba-114">Указатель на буфер памяти, выделенный вызывающим объектом, *длиной* размера.</span><span class="sxs-lookup"><span data-stu-id="db6ba-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span> <span data-ttu-id="db6ba-115">Буфер должен содержать аппаратно-независимый точечный рисунок GDI (DIB).</span><span class="sxs-lookup"><span data-stu-id="db6ba-115">The buffer should contain a GDI device-independent bitmap (DIB).</span></span>

</dd> <dt>

<span data-ttu-id="db6ba-116">*length*</span><span class="sxs-lookup"><span data-stu-id="db6ba-116">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="db6ba-117">Длина буфера.</span><span class="sxs-lookup"><span data-stu-id="db6ba-117">Length of the buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db6ba-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db6ba-118">Remarks</span></span>

<span data-ttu-id="db6ba-119">Класс [**Цимажеаллокатор**](cimageallocator.md) создает DIB с помощью объекта сопоставления файлов, поддерживаемого файлом подкачки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="db6ba-119">The [**CImageAllocator**](cimageallocator.md) class creates a DIB using a file-mapping object that is backed by the operating-system paging file.</span></span> <span data-ttu-id="db6ba-120">Маркер объекта сопоставления файлов хранится в элементе **хмаппинг** структуры **\_ дибдата m** .</span><span class="sxs-lookup"><span data-stu-id="db6ba-120">The handle to the file-mapping object is stored in the **hMapping** member of the **m\_DibData** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="db6ba-121">Требования</span><span class="sxs-lookup"><span data-stu-id="db6ba-121">Requirements</span></span>



| <span data-ttu-id="db6ba-122">Требование</span><span class="sxs-lookup"><span data-stu-id="db6ba-122">Requirement</span></span> | <span data-ttu-id="db6ba-123">Значение</span><span class="sxs-lookup"><span data-stu-id="db6ba-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db6ba-124">Header</span><span class="sxs-lookup"><span data-stu-id="db6ba-124">Header</span></span><br/>  | <dl> <span data-ttu-id="db6ba-125"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db6ba-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="db6ba-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="db6ba-126">Library</span></span><br/> | <dl> <span data-ttu-id="db6ba-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="db6ba-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db6ba-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db6ba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db6ba-129">**Класс Цимажесампле**</span><span class="sxs-lookup"><span data-stu-id="db6ba-129">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




