---
description: 'Кбасефилтер. Финдпин, метод Финдпин извлекает ПИН-код с указанным идентификатором. Этот метод реализует метод Ибасефилтер:: Финдпин.'
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: Кбасефилтер. Финдпин, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2bbef9b051a42597b2585a432f544eead4e2e0a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099822"
---
# <a name="cbasefilterfindpin-method"></a><span data-ttu-id="c422d-104">Кбасефилтер. Финдпин, метод</span><span class="sxs-lookup"><span data-stu-id="c422d-104">CBaseFilter.FindPin method</span></span>

<span data-ttu-id="c422d-105">`FindPin`Метод извлекает ПИН-код с указанным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="c422d-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="c422d-106">Этот метод реализует метод [**ибасефилтер:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="c422d-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c422d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c422d-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="c422d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c422d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c422d-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="c422d-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="c422d-110">Указатель на константу, заканчивающуюся нулем строкой Юникода, которая идентифицирует ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="c422d-110">Pointer to a constant, null-terminated Unicode string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="c422d-111">*пппин*</span><span class="sxs-lookup"><span data-stu-id="c422d-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="c422d-112">Адрес переменной, которая получает указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="c422d-112">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c422d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c422d-113">Return value</span></span>

<span data-ttu-id="c422d-114">Возвращает одно из следующих значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c422d-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="c422d-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c422d-115">Return code</span></span>                                                                                       | <span data-ttu-id="c422d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c422d-116">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="c422d-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c422d-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="c422d-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c422d-118">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="c422d-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="c422d-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="c422d-120">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="c422d-120">**NULL** pointer argument.</span></span><br/>     |
| <dl> <span data-ttu-id="c422d-121"><dt>**VFW \_ E \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="c422d-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="c422d-122">Не удалось найти соответствующий ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="c422d-122">Could not find a matching pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c422d-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="c422d-123">Remarks</span></span>

<span data-ttu-id="c422d-124">Этот метод вызывает метод [**кбасепин:: Name**](cbasepin-name.md) для сравнения имени каждого контакта со строкой, заданной параметром *ID* .</span><span class="sxs-lookup"><span data-stu-id="c422d-124">This method calls the [**CBasePin::Name**](cbasepin-name.md) method to compare each pin's name against the string specified by the *Id* parameter.</span></span>

<span data-ttu-id="c422d-125">Если метод выполнен успешно, то интерфейс **Ипин** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="c422d-125">If the method succeeds, the **IPin** interface has an outstanding reference count.</span></span> <span data-ttu-id="c422d-126">Не забудьте освободить его по завершении.</span><span class="sxs-lookup"><span data-stu-id="c422d-126">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="c422d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c422d-127">Requirements</span></span>



| <span data-ttu-id="c422d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c422d-128">Requirement</span></span> | <span data-ttu-id="c422d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c422d-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c422d-130">Header</span><span class="sxs-lookup"><span data-stu-id="c422d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c422d-131"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c422d-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c422d-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c422d-132">Library</span></span><br/> | <dl> <span data-ttu-id="c422d-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c422d-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c422d-134">См. также</span><span class="sxs-lookup"><span data-stu-id="c422d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c422d-135">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="c422d-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




