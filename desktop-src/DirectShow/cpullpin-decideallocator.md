---
description: Метод ДеЦидеаллокатор согласовывает распределитель с выходным закреплением.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: Кпуллпин. ДеЦидеаллокатор, метод (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91ffa139b916b1594e0729a0f8d52f07c62eda12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679652"
---
# <a name="cpullpindecideallocator-method"></a><span data-ttu-id="d6d9c-103">Кпуллпин. ДеЦидеаллокатор, метод</span><span class="sxs-lookup"><span data-stu-id="d6d9c-103">CPullPin.DecideAllocator method</span></span>

<span data-ttu-id="d6d9c-104">`DecideAllocator`Метод согласовывает распределитель с выходным закреплением.</span><span class="sxs-lookup"><span data-stu-id="d6d9c-104">The `DecideAllocator` method negotiates an allocator with the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d9c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6d9c-105">Syntax</span></span>


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="d6d9c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6d9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6d9c-107">*паллок*</span><span class="sxs-lookup"><span data-stu-id="d6d9c-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="d6d9c-108">Указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) предпочтительного распределителя входного контакта или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d6d9c-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the input pin's preferred allocator, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d6d9c-109">*ппропс*</span><span class="sxs-lookup"><span data-stu-id="d6d9c-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="d6d9c-110">Указатель на необязательную [**структуру \_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , которая содержит требования к буферу входного контакта.</span><span class="sxs-lookup"><span data-stu-id="d6d9c-110">Pointer to an optional [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6d9c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6d9c-111">Return value</span></span>

<span data-ttu-id="d6d9c-112">Возвращает \_ ОК, если успешно, или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d6d9c-112">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6d9c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6d9c-113">Remarks</span></span>

<span data-ttu-id="d6d9c-114">Этот метод вызывает метод [**иасинкреадер:: рекуесталлокатор**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) для согласования распределителя.</span><span class="sxs-lookup"><span data-stu-id="d6d9c-114">This method calls the [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) method to negotiate an allocator.</span></span> <span data-ttu-id="d6d9c-115">Он передает параметр *паллок* непосредственно в метод **рекуесталлокатор** .</span><span class="sxs-lookup"><span data-stu-id="d6d9c-115">It passes the *pAlloc* parameter directly to the **RequestAllocator** method.</span></span> <span data-ttu-id="d6d9c-116">Он передает параметр *ппропс* в **Рекуесталлокатор** , если *ппропс* имеет значение, отличное от **null**. в противном случае он создает структуру **\_ свойств распределителя** с запросом по умолчанию из трех буферов размером 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="d6d9c-116">It passes the *pProps* parameter to **RequestAllocator** if *pProps* is non-**NULL**; otherwise, it creates an **ALLOCATOR\_PROPERTIES** structure with a default request of three 64K buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6d9c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d6d9c-117">Requirements</span></span>



| <span data-ttu-id="d6d9c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d6d9c-118">Requirement</span></span> | <span data-ttu-id="d6d9c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d6d9c-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d9c-120">Header</span><span class="sxs-lookup"><span data-stu-id="d6d9c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d6d9c-121"><dt>Пуллпин. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6d9c-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="d6d9c-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d6d9c-122">Library</span></span><br/> | <dl> <span data-ttu-id="d6d9c-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d6d9c-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6d9c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6d9c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d9c-125">**Класс Кпуллпин**</span><span class="sxs-lookup"><span data-stu-id="d6d9c-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> <dt>

[<span data-ttu-id="d6d9c-126">**Кпуллпин:: Connect**</span><span class="sxs-lookup"><span data-stu-id="d6d9c-126">**CPullPin::Connect**</span></span>](cpullpin-connect.md)
</dt> </dl>

 

 




