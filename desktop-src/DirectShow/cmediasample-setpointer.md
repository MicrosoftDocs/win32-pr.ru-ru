---
description: Метод Сетпоинтер задает указатель на буфер памяти.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: Кмедиасампле. Сетпоинтер, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67d9fc5d260cc627919a458593328c36f0de9a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674981"
---
# <a name="cmediasamplesetpointer-method"></a><span data-ttu-id="a2d68-103">Кмедиасампле. Сетпоинтер, метод</span><span class="sxs-lookup"><span data-stu-id="a2d68-103">CMediaSample.SetPointer method</span></span>

<span data-ttu-id="a2d68-104">`SetPointer`Метод задает указатель на буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="a2d68-104">The `SetPointer` method sets the pointer to the memory buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2d68-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2d68-105">Syntax</span></span>


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="a2d68-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2d68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2d68-107">*ptr*</span><span class="sxs-lookup"><span data-stu-id="a2d68-107">*ptr*</span></span> 
</dt> <dd>

<span data-ttu-id="a2d68-108">Указатель на буфер памяти, выделенный вызывающей стороной размера *кбитес*.</span><span class="sxs-lookup"><span data-stu-id="a2d68-108">Pointer to a memory buffer allocated by the caller, of size *cBytes*.</span></span>

</dd> <dt>

<span data-ttu-id="a2d68-109">*кбитес*</span><span class="sxs-lookup"><span data-stu-id="a2d68-109">*cBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="a2d68-110">Длина буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="a2d68-110">Length of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2d68-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2d68-111">Return value</span></span>

<span data-ttu-id="a2d68-112">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a2d68-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2d68-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2d68-113">Remarks</span></span>

<span data-ttu-id="a2d68-114">Этот метод позволяет распределительу установить новый указатель для образца.</span><span class="sxs-lookup"><span data-stu-id="a2d68-114">This method enables the allocator to set a new pointer for the sample.</span></span>

<span data-ttu-id="a2d68-115">Этот метод недоступен через интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="a2d68-115">This method is not available through the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="a2d68-116">Объект, создающий образец, может получить доступ к этому методу (через **кмедиасампле**), но другие объекты не могут.</span><span class="sxs-lookup"><span data-stu-id="a2d68-116">The object that creates the sample can access this method (through **CMediaSample**), but other objects cannot.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2d68-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a2d68-117">Requirements</span></span>



| <span data-ttu-id="a2d68-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a2d68-118">Requirement</span></span> | <span data-ttu-id="a2d68-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a2d68-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2d68-120">Header</span><span class="sxs-lookup"><span data-stu-id="a2d68-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a2d68-121"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2d68-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a2d68-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a2d68-122">Library</span></span><br/> | <dl> <span data-ttu-id="a2d68-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a2d68-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2d68-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2d68-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2d68-125">**Класс Кмедиасампле**</span><span class="sxs-lookup"><span data-stu-id="a2d68-125">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




