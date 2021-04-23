---
description: Метод Иниталлокатор создает механизм выделения памяти.
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: CBaseOutputPin.Iniметод Таллокатор (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.InitAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e5385671ba4c7fdf1b719f83aafba7d84421bce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669173"
---
# <a name="cbaseoutputpininitallocator-method"></a><span data-ttu-id="7662a-103">CBaseOutputPin.Iniметод Таллокатор</span><span class="sxs-lookup"><span data-stu-id="7662a-103">CBaseOutputPin.InitAllocator method</span></span>

<span data-ttu-id="7662a-104">`InitAllocator`Метод создает механизм выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="7662a-104">The `InitAllocator` method creates a memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="7662a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7662a-105">Syntax</span></span>


```C++
virtual HRESULT InitAllocator(
   IMemAllocator **ppAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="7662a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7662a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7662a-107">*ппаллок*</span><span class="sxs-lookup"><span data-stu-id="7662a-107">*ppAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="7662a-108">Адрес переменной, которая получает указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя.</span><span class="sxs-lookup"><span data-stu-id="7662a-108">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7662a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7662a-109">Return value</span></span>

<span data-ttu-id="7662a-110">Возвращает \_ ОК в случае успеха или код ошибки из функции **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="7662a-110">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="7662a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7662a-111">Remarks</span></span>

<span data-ttu-id="7662a-112">Если входной ПИН-код не предоставляет распределитель памяти, метод [**кбасеаутпутпин::D еЦидеаллокатор**](cbaseoutputpin-decideallocator.md) вызывает этот метод для создания распределителя.</span><span class="sxs-lookup"><span data-stu-id="7662a-112">If the input pin does not provide a memory allocator, the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method calls this method to create an allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="7662a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7662a-113">Requirements</span></span>



| <span data-ttu-id="7662a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7662a-114">Requirement</span></span> | <span data-ttu-id="7662a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7662a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7662a-116">Header</span><span class="sxs-lookup"><span data-stu-id="7662a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7662a-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7662a-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7662a-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7662a-118">Library</span></span><br/> | <dl> <span data-ttu-id="7662a-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7662a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7662a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7662a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7662a-121">**Класс Кбасеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="7662a-121">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




