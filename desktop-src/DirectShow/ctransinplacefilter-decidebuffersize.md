---
description: Метод ДеЦидебуфферсизе задает требования к буферу выходного контакта.
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: Ктрансинплацефилтер. ДеЦидебуфферсизе, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55227510eee3c1afdcd14ed390edf21eccfcf1de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675197"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a><span data-ttu-id="07b25-103">Ктрансинплацефилтер. ДеЦидебуфферсизе, метод</span><span class="sxs-lookup"><span data-stu-id="07b25-103">CTransInPlaceFilter.DecideBufferSize method</span></span>

<span data-ttu-id="07b25-104">`DecideBufferSize`Метод задает требования к буферу выходного контакта.</span><span class="sxs-lookup"><span data-stu-id="07b25-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="07b25-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07b25-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a><span data-ttu-id="07b25-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="07b25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07b25-107">*паллок*</span><span class="sxs-lookup"><span data-stu-id="07b25-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="07b25-108">Указатель на объект [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) , используемый выходным закреплением.</span><span class="sxs-lookup"><span data-stu-id="07b25-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) object used by the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="07b25-109">*pProperties*</span><span class="sxs-lookup"><span data-stu-id="07b25-109">*pProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="07b25-110">Указатель на запрошенные свойства распределителя для счетчика, размера и выравнивания, как указано в [**структуре \_ свойств распределителя**](/windows/win32/api/strmif/ns-strmif-allocator_properties) .</span><span class="sxs-lookup"><span data-stu-id="07b25-110">Pointer to the requested allocator properties for count, size, and alignment, as specified by the [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07b25-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07b25-111">Return value</span></span>

<span data-ttu-id="07b25-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07b25-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="07b25-113">Возможные значения включают в себя, показанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="07b25-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="07b25-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="07b25-114">Return code</span></span>                                                                            | <span data-ttu-id="07b25-115">Описание</span><span class="sxs-lookup"><span data-stu-id="07b25-115">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="07b25-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="07b25-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="07b25-117">Успешно</span><span class="sxs-lookup"><span data-stu-id="07b25-117">Success</span></span><br/> |
| <dl> <span data-ttu-id="07b25-118"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="07b25-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="07b25-119">Failure</span><span class="sxs-lookup"><span data-stu-id="07b25-119">Failure</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="07b25-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07b25-120">Remarks</span></span>

<span data-ttu-id="07b25-121">Этот метод вызывается, когда классу **ктрансинплацефилтер** требуется предоставить размер буфера для подчиненного фильтра.</span><span class="sxs-lookup"><span data-stu-id="07b25-121">This method is called when the **CTransInPlaceFilter** class needs to provide a buffer size to the downstream filter.</span></span> <span data-ttu-id="07b25-122">Если фильтр **ктрансинплацефилтер** уже подключился к вышестоящему потоку, он использует свойства распределителя для вышестоящего подключения.</span><span class="sxs-lookup"><span data-stu-id="07b25-122">If the **CTransInPlaceFilter** filter is already connected upstream, it uses the allocator properties on the upstream pin connection.</span></span> <span data-ttu-id="07b25-123">В противном случае размер буфера устанавливается в 1 байт в качестве временного значения заполнителя.</span><span class="sxs-lookup"><span data-stu-id="07b25-123">Otherwise, it sets the buffer size to 1 byte as a temporary place-holder value.</span></span> <span data-ttu-id="07b25-124">При соединении вышестоящего фильтра класс **ктрансинплацефилтер** повторно согласовывает нисходящий распределитель.</span><span class="sxs-lookup"><span data-stu-id="07b25-124">When the upstream filter connects, the **CTransInPlaceFilter** class renegotiates the downstream allocator.</span></span> <span data-ttu-id="07b25-125">Дополнительные сведения о процессе подключения ПИН-кода в этом классе см. в разделе [**класс ктрансинплацефилтер**](ctransinplacefilter.md).</span><span class="sxs-lookup"><span data-stu-id="07b25-125">For more information about the pin connection process in this class, see [**CTransInPlaceFilter Class**](ctransinplacefilter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07b25-126">Требования</span><span class="sxs-lookup"><span data-stu-id="07b25-126">Requirements</span></span>



| <span data-ttu-id="07b25-127">Требование</span><span class="sxs-lookup"><span data-stu-id="07b25-127">Requirement</span></span> | <span data-ttu-id="07b25-128">Значение</span><span class="sxs-lookup"><span data-stu-id="07b25-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b25-129">Header</span><span class="sxs-lookup"><span data-stu-id="07b25-129">Header</span></span><br/>  | <dl> <span data-ttu-id="07b25-130"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07b25-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="07b25-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="07b25-131">Library</span></span><br/> | <dl> <span data-ttu-id="07b25-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="07b25-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07b25-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07b25-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b25-134">**Класс Ктрансинплацефилтер**</span><span class="sxs-lookup"><span data-stu-id="07b25-134">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




