---
description: Метод Креатедиб создает независимый от устройства точечный рисунок GDI (DIB). DIB выделяется в общем блоке мемпори, который удаляет операцию копирования, когда фильтр-владелец блитс изображение.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: Цимажеаллокатор. Креатедиб, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateDIB
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 316b7aeadfa442a8df4e80075380464758f3c6bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675828"
---
# <a name="cimageallocatorcreatedib-method"></a><span data-ttu-id="36a1b-104">Цимажеаллокатор. Креатедиб, метод</span><span class="sxs-lookup"><span data-stu-id="36a1b-104">CImageAllocator.CreateDIB method</span></span>

<span data-ttu-id="36a1b-105">`CreateDIB`Метод создает аппаратно-независимый точечный рисунок GDI (DIB).</span><span class="sxs-lookup"><span data-stu-id="36a1b-105">The `CreateDIB` method creates a GDI device-independent bitmap (DIB).</span></span> <span data-ttu-id="36a1b-106">DIB выделяется в общем блоке мемпори, который удаляет операцию копирования, когда фильтр-владелец блитс изображение.</span><span class="sxs-lookup"><span data-stu-id="36a1b-106">The DIB is allocated in a shared mempory block, which eliminates a copy operation when the owning filter blits the image.</span></span>

## <a name="syntax"></a><span data-ttu-id="36a1b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36a1b-107">Syntax</span></span>


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a><span data-ttu-id="36a1b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="36a1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36a1b-109">*Неразмерность*</span><span class="sxs-lookup"><span data-stu-id="36a1b-109">*InSize*</span></span> 
</dt> <dd>

<span data-ttu-id="36a1b-110">Размер точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="36a1b-110">Size of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="36a1b-111">*Дибдата* \[ ЗНАЧ\]</span><span class="sxs-lookup"><span data-stu-id="36a1b-111">*DibData* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="36a1b-112">Ссылка на структуру [**дибдата**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="36a1b-112">Reference to a [**DIBDATA**](dibdata.md) structure.</span></span> <span data-ttu-id="36a1b-113">Метод заполняет эту структуру сведениями об элементе DIB.</span><span class="sxs-lookup"><span data-stu-id="36a1b-113">The method fills in this structure with information about the DIB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36a1b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36a1b-114">Return value</span></span>

<span data-ttu-id="36a1b-115">Возвращает \_ ОК, если успешно, или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="36a1b-115">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="36a1b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="36a1b-116">Requirements</span></span>



| <span data-ttu-id="36a1b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="36a1b-117">Requirement</span></span> | <span data-ttu-id="36a1b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="36a1b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36a1b-119">Header</span><span class="sxs-lookup"><span data-stu-id="36a1b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="36a1b-120"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36a1b-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="36a1b-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="36a1b-121">Library</span></span><br/> | <dl> <span data-ttu-id="36a1b-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="36a1b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36a1b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36a1b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36a1b-124">**Класс Цимажеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="36a1b-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> <dt>

[<span data-ttu-id="36a1b-125">**Цимажеаллокатор:: Alloc**</span><span class="sxs-lookup"><span data-stu-id="36a1b-125">**CImageAllocator::Alloc**</span></span>](cimageallocator-alloc.md)
</dt> </dl>

 

 




