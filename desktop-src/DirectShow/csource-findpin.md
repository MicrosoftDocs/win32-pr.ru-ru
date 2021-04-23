---
description: 'Метод Финдпин извлекает ПИН-код с указанным идентификатором. Этот метод реализует метод Ибасефилтер:: Финдпин.'
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: Метод Ксаурце. Финдпин (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fac8df1e53e4a129b42d1284a19392bc7b58aa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665139"
---
# <a name="csourcefindpin-method"></a><span data-ttu-id="a1bdc-104">Ксаурце. Финдпин, метод</span><span class="sxs-lookup"><span data-stu-id="a1bdc-104">CSource.FindPin method</span></span>

<span data-ttu-id="a1bdc-105">`FindPin`Метод извлекает ПИН-код с указанным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="a1bdc-106">Этот метод реализует метод [**ибасефилтер:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="a1bdc-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1bdc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1bdc-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="a1bdc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1bdc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1bdc-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="a1bdc-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="a1bdc-110">Указатель на строку, завершающуюся нулем, которая определяет ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-110">Pointer to a null-terminated string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="a1bdc-111">*пппин*</span><span class="sxs-lookup"><span data-stu-id="a1bdc-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="a1bdc-112">Получает указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="a1bdc-113">Если метод завершается с ошибкой, \* *пппин* имеет значение **null** .</span><span class="sxs-lookup"><span data-stu-id="a1bdc-113">If the method fails, \**ppPin* is set to **NULL**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1bdc-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1bdc-114">Return value</span></span>

<span data-ttu-id="a1bdc-115">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a1bdc-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a1bdc-116">Return code</span></span>                                                                                       | <span data-ttu-id="a1bdc-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a1bdc-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="a1bdc-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a1bdc-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="a1bdc-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a1bdc-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="a1bdc-120"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="a1bdc-121">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-121">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="a1bdc-122"><dt>**VFW \_ E \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="a1bdc-122"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="a1bdc-123">Не удалось найти ПИН-код с этим идентификатором.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-123">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a1bdc-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1bdc-124">Remarks</span></span>

<span data-ttu-id="a1bdc-125">Первый ПИН-код всегда имеет имя "1"; второй ПИН-код называется "2"; и т. д.</span><span class="sxs-lookup"><span data-stu-id="a1bdc-125">The first pin is always named "1"; the second pin is named "2"; and so forth.</span></span> <span data-ttu-id="a1bdc-126">Дополнительные сведения см. в разделе [**ксаурцестреам:: QueryId**](csourcestream-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="a1bdc-126">For more information, see [**CSourceStream::QueryId**](csourcestream-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1bdc-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a1bdc-127">Requirements</span></span>



| <span data-ttu-id="a1bdc-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a1bdc-128">Requirement</span></span> | <span data-ttu-id="a1bdc-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a1bdc-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1bdc-130">Header</span><span class="sxs-lookup"><span data-stu-id="a1bdc-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a1bdc-131"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1bdc-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a1bdc-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a1bdc-132">Library</span></span><br/> | <dl> <span data-ttu-id="a1bdc-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a1bdc-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1bdc-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1bdc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1bdc-135">**Класс Ксаурце**</span><span class="sxs-lookup"><span data-stu-id="a1bdc-135">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




