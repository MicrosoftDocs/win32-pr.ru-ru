---
description: Метод метода распределителе извлекает распределитель памяти, предложенный этим ПИН-кодом. Этот метод реализует метод Имеминпутпин::/распределителя.
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Метод Кбасеинпутпин. методом перераспределения (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 098738fc63ba1834b1eefb4b2518e3309db35c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657066"
---
# <a name="cbaseinputpingetallocator-method"></a><span data-ttu-id="8333c-104">Кбасеинпутпин. метод распределения</span><span class="sxs-lookup"><span data-stu-id="8333c-104">CBaseInputPin.GetAllocator method</span></span>

<span data-ttu-id="8333c-105">`GetAllocator`Метод извлекает распределитель памяти, предложенный этим ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="8333c-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="8333c-106">Этот метод реализует метод [**имеминпутпин::/распределителя**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .</span><span class="sxs-lookup"><span data-stu-id="8333c-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8333c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8333c-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="8333c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8333c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8333c-109">*ппаллокатор*</span><span class="sxs-lookup"><span data-stu-id="8333c-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="8333c-110">Адрес переменной, которая получает указатель на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя.</span><span class="sxs-lookup"><span data-stu-id="8333c-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8333c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8333c-111">Return value</span></span>

<span data-ttu-id="8333c-112">Возвращает \_ ОК в случае успеха или код ошибки из функции **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="8333c-112">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="8333c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8333c-113">Remarks</span></span>

<span data-ttu-id="8333c-114">Этот метод создает объект [**кмемаллокатор**](cmemallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="8333c-114">This method creates a [**CMemAllocator**](cmemallocator.md) object.</span></span> <span data-ttu-id="8333c-115">Переопределите этот метод, если фильтр использует распределитель из подчиненного ПИН-кода или пользовательского распределителя.</span><span class="sxs-lookup"><span data-stu-id="8333c-115">Override this method if your filter uses an allocator from a downstream pin, or a custom allocator.</span></span>

<span data-ttu-id="8333c-116">Если метод выполнен успешно, то интерфейс **имемаллокатор** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="8333c-116">If the method succeeds, the **IMemAllocator** interface has an outstanding reference count.</span></span> <span data-ttu-id="8333c-117">Не забудьте освободить его по завершении.</span><span class="sxs-lookup"><span data-stu-id="8333c-117">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="8333c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8333c-118">Requirements</span></span>



| <span data-ttu-id="8333c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8333c-119">Requirement</span></span> | <span data-ttu-id="8333c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8333c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8333c-121">Header</span><span class="sxs-lookup"><span data-stu-id="8333c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8333c-122"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8333c-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8333c-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8333c-123">Library</span></span><br/> | <dl> <span data-ttu-id="8333c-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8333c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8333c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8333c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8333c-126">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="8333c-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




