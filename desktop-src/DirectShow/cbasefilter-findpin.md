---
description: 'Метод Финдпин извлекает ПИН-код с указанным идентификатором. Этот метод реализует метод Ибасефилтер:: Финдпин.'
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
ms.openlocfilehash: 98b49c547ec59a74185f7f719da660220de8480f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657684"
---
# <a name="cbasefilterfindpin-method"></a><span data-ttu-id="a8b95-104">Кбасефилтер. Финдпин, метод</span><span class="sxs-lookup"><span data-stu-id="a8b95-104">CBaseFilter.FindPin method</span></span>

<span data-ttu-id="a8b95-105">`FindPin`Метод извлекает ПИН-код с указанным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="a8b95-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="a8b95-106">Этот метод реализует метод [**ибасефилтер:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="a8b95-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b95-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8b95-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="a8b95-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8b95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b95-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="a8b95-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="a8b95-110">Указатель на константу, заканчивающуюся нулем строкой Юникода, которая идентифицирует ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="a8b95-110">Pointer to a constant, null-terminated Unicode string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="a8b95-111">*пппин*</span><span class="sxs-lookup"><span data-stu-id="a8b95-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="a8b95-112">Адрес переменной, которая получает указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="a8b95-112">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b95-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8b95-113">Return value</span></span>

<span data-ttu-id="a8b95-114">Возвращает одно из следующих значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8b95-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="a8b95-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a8b95-115">Return code</span></span>                                                                                       | <span data-ttu-id="a8b95-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a8b95-116">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="a8b95-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a8b95-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="a8b95-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="a8b95-118">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="a8b95-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="a8b95-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="a8b95-120">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="a8b95-120">**NULL** pointer argument.</span></span><br/>     |
| <dl> <span data-ttu-id="a8b95-121"><dt>**VFW \_ E \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="a8b95-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="a8b95-122">Не удалось найти соответствующий ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="a8b95-122">Could not find a matching pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a8b95-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8b95-123">Remarks</span></span>

<span data-ttu-id="a8b95-124">Этот метод вызывает метод [**кбасепин:: Name**](cbasepin-name.md) для сравнения имени каждого контакта со строкой, заданной параметром *ID* .</span><span class="sxs-lookup"><span data-stu-id="a8b95-124">This method calls the [**CBasePin::Name**](cbasepin-name.md) method to compare each pin's name against the string specified by the *Id* parameter.</span></span>

<span data-ttu-id="a8b95-125">Если метод выполнен успешно, то интерфейс **Ипин** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="a8b95-125">If the method succeeds, the **IPin** interface has an outstanding reference count.</span></span> <span data-ttu-id="a8b95-126">Не забудьте освободить его по завершении.</span><span class="sxs-lookup"><span data-stu-id="a8b95-126">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b95-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a8b95-127">Requirements</span></span>



| <span data-ttu-id="a8b95-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a8b95-128">Requirement</span></span> | <span data-ttu-id="a8b95-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a8b95-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b95-130">Header</span><span class="sxs-lookup"><span data-stu-id="a8b95-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a8b95-131"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8b95-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a8b95-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a8b95-132">Library</span></span><br/> | <dl> <span data-ttu-id="a8b95-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a8b95-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b95-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8b95-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b95-135">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="a8b95-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




