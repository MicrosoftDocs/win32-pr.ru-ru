---
description: Метод Финдпин извлекает ПИН-код с указанным идентификатором.
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: Кбасерендерер. Финдпин, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6e6789a91f34d95933ae7869e1588eeb14b6006
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668741"
---
# <a name="cbaserendererfindpin-method"></a><span data-ttu-id="7eefe-103">Кбасерендерер. Финдпин, метод</span><span class="sxs-lookup"><span data-stu-id="7eefe-103">CBaseRenderer.FindPin method</span></span>

<span data-ttu-id="7eefe-104">`FindPin`Метод извлекает ПИН-код с указанным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="7eefe-104">The `FindPin` method retrieves the pin with the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eefe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7eefe-105">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="7eefe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7eefe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eefe-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="7eefe-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="7eefe-108">Указатель на константу, заканчивающуюся нулем строкой расширенных символов, определяющую ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="7eefe-108">Pointer to a constant, null-terminated wide-character string that identifies the pin.</span></span> <span data-ttu-id="7eefe-109">Должен быть L "in".</span><span class="sxs-lookup"><span data-stu-id="7eefe-109">Must be L"In".</span></span>

</dd> <dt>

<span data-ttu-id="7eefe-110">*пппин*</span><span class="sxs-lookup"><span data-stu-id="7eefe-110">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="7eefe-111">Адрес переменной, которая получает указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="7eefe-111">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="7eefe-112">Если метод завершается с ошибкой, *\* пппин* имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="7eefe-112">If the method fails, *\*ppPin* is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eefe-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7eefe-113">Return value</span></span>

<span data-ttu-id="7eefe-114">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7eefe-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="7eefe-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7eefe-115">Return code</span></span>                                                                                       | <span data-ttu-id="7eefe-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7eefe-116">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="7eefe-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7eefe-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="7eefe-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="7eefe-118">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="7eefe-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="7eefe-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="7eefe-120">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="7eefe-120">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="7eefe-121"><dt>**VFW \_ E \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="7eefe-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="7eefe-122">Не найдено.</span><span class="sxs-lookup"><span data-stu-id="7eefe-122">Not found.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="7eefe-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7eefe-123">Remarks</span></span>

<span data-ttu-id="7eefe-124">Этот метод переопределяет метод [**кбасефилтер:: финдпин**](cbasefilter-findpin.md) .</span><span class="sxs-lookup"><span data-stu-id="7eefe-124">This method overrides the [**CBaseFilter::FindPin**](cbasefilter-findpin.md) method.</span></span> <span data-ttu-id="7eefe-125">ПИН-код фильтра (входной ПИН-код) называется "in".</span><span class="sxs-lookup"><span data-stu-id="7eefe-125">The filter's only pin (the input pin) is named "In".</span></span>

## <a name="requirements"></a><span data-ttu-id="7eefe-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7eefe-126">Requirements</span></span>



| <span data-ttu-id="7eefe-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7eefe-127">Requirement</span></span> | <span data-ttu-id="7eefe-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7eefe-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eefe-129">Header</span><span class="sxs-lookup"><span data-stu-id="7eefe-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7eefe-130"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7eefe-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7eefe-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7eefe-131">Library</span></span><br/> | <dl> <span data-ttu-id="7eefe-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7eefe-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eefe-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7eefe-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eefe-134">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="7eefe-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




