---
description: Метод конструктора Цимажесампле. Цимажесампле.
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
ms.openlocfilehash: ecab52e347e03b698adccb79b77da879d26612b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095612"
---
# <a name="cimagesamplecimagesample-constructor"></a><span data-ttu-id="5b376-103">Цимажесампле. Цимажесампле, конструктор</span><span class="sxs-lookup"><span data-stu-id="5b376-103">CImageSample.CImageSample constructor</span></span>

<span data-ttu-id="5b376-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="5b376-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b376-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b376-105">Syntax</span></span>


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a><span data-ttu-id="5b376-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b376-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b376-107">*паллокатор*</span><span class="sxs-lookup"><span data-stu-id="5b376-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="5b376-108">Указатель на распределитель, создавший этот образец.</span><span class="sxs-lookup"><span data-stu-id="5b376-108">Pointer to the allocator that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="5b376-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="5b376-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="5b376-110">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="5b376-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="5b376-111">*фр*</span><span class="sxs-lookup"><span data-stu-id="5b376-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="5b376-112">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="5b376-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="5b376-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="5b376-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="5b376-114">Указатель на буфер памяти, выделенный вызывающим объектом, *длиной* размера.</span><span class="sxs-lookup"><span data-stu-id="5b376-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span> <span data-ttu-id="5b376-115">Буфер должен содержать аппаратно-независимый точечный рисунок GDI (DIB).</span><span class="sxs-lookup"><span data-stu-id="5b376-115">The buffer should contain a GDI device-independent bitmap (DIB).</span></span>

</dd> <dt>

<span data-ttu-id="5b376-116">*length*</span><span class="sxs-lookup"><span data-stu-id="5b376-116">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="5b376-117">Длина буфера.</span><span class="sxs-lookup"><span data-stu-id="5b376-117">Length of the buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b376-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="5b376-118">Remarks</span></span>

<span data-ttu-id="5b376-119">Класс [**Цимажеаллокатор**](cimageallocator.md) создает DIB с помощью объекта сопоставления файлов, поддерживаемого файлом подкачки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5b376-119">The [**CImageAllocator**](cimageallocator.md) class creates a DIB using a file-mapping object that is backed by the operating-system paging file.</span></span> <span data-ttu-id="5b376-120">Маркер объекта сопоставления файлов хранится в элементе **хмаппинг** структуры **\_ дибдата m** .</span><span class="sxs-lookup"><span data-stu-id="5b376-120">The handle to the file-mapping object is stored in the **hMapping** member of the **m\_DibData** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b376-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5b376-121">Requirements</span></span>



| <span data-ttu-id="5b376-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5b376-122">Requirement</span></span> | <span data-ttu-id="5b376-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5b376-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b376-124">Header</span><span class="sxs-lookup"><span data-stu-id="5b376-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5b376-125"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b376-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5b376-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5b376-126">Library</span></span><br/> | <dl> <span data-ttu-id="5b376-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5b376-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b376-128">См. также</span><span class="sxs-lookup"><span data-stu-id="5b376-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b376-129">**Класс Цимажесампле**</span><span class="sxs-lookup"><span data-stu-id="5b376-129">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




