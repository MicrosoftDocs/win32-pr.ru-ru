---
description: 'Метод Финдпин получает ПИН-код с указанным идентификатором. Этот метод реализует метод Ибасефилтер:: Финдпин.'
ms.assetid: 56ee3e0d-9e3f-4d25-846b-50119b55a122
title: Ктрансформфилтер. Финдпин, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1631651932d5adbc49fb59d44291dccea55fd41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657343"
---
# <a name="ctransformfilterfindpin-method"></a><span data-ttu-id="5920c-104">Ктрансформфилтер. Финдпин, метод</span><span class="sxs-lookup"><span data-stu-id="5920c-104">CTransformFilter.FindPin method</span></span>

<span data-ttu-id="5920c-105">Метод **финдпин** получает ПИН-код с указанным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="5920c-105">The **FindPin** method gets the pin with the specified identifier.</span></span> <span data-ttu-id="5920c-106">Этот метод реализует метод [**ибасефилтер:: финдпин**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .</span><span class="sxs-lookup"><span data-stu-id="5920c-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5920c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5920c-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="5920c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5920c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5920c-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="5920c-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="5920c-110">Строка расширенных символов, содержащая идентификатор ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="5920c-110">Wide-character string that contains the pin identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5920c-111">*пппин*</span><span class="sxs-lookup"><span data-stu-id="5920c-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="5920c-112">Получает указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="5920c-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="5920c-113">Если метод завершается с ошибкой, `*ppPin` устанавливается в **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5920c-113">If the method fails, `*ppPin` is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5920c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5920c-114">Return value</span></span>

<span data-ttu-id="5920c-115">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5920c-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="5920c-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5920c-116">Return code</span></span>                                                                                       | <span data-ttu-id="5920c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="5920c-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="5920c-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5920c-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="5920c-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="5920c-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5920c-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5920c-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="5920c-121">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="5920c-121">Insufficient memory.</span></span><br/>                       |
| <dl> <span data-ttu-id="5920c-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="5920c-122"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="5920c-123">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="5920c-123">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="5920c-124"><dt>**VFW \_ E \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="5920c-124"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="5920c-125">Не удалось найти ПИН-код с этим идентификатором.</span><span class="sxs-lookup"><span data-stu-id="5920c-125">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5920c-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5920c-126">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5920c-127">Реализация этого метода не вызывает [**Ипин:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) для сопоставления с идентификатором ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="5920c-127">The implementation of this method does not call [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) to match the pin identifier.</span></span> <span data-ttu-id="5920c-128">Вместо этого метод предполагает, что входной ПИН-код имеет имя in, а выходной ПИН-код имеет имя out.</span><span class="sxs-lookup"><span data-stu-id="5920c-128">Instead, the method assumes that the input pin is named "In", and the output pin is named "Out".</span></span> <span data-ttu-id="5920c-129">Если используется другой набор ПИН-кодов, Переопределите этот метод.</span><span class="sxs-lookup"><span data-stu-id="5920c-129">If you use a different set of pin identifiers, override this method.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5920c-130">Требования</span><span class="sxs-lookup"><span data-stu-id="5920c-130">Requirements</span></span>



| <span data-ttu-id="5920c-131">Требование</span><span class="sxs-lookup"><span data-stu-id="5920c-131">Requirement</span></span> | <span data-ttu-id="5920c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5920c-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5920c-133">Header</span><span class="sxs-lookup"><span data-stu-id="5920c-133">Header</span></span><br/>  | <dl> <span data-ttu-id="5920c-134"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5920c-134"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5920c-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5920c-135">Library</span></span><br/> | <dl> <span data-ttu-id="5920c-136"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5920c-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5920c-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5920c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5920c-138">**Класс Ктрансформфилтер**</span><span class="sxs-lookup"><span data-stu-id="5920c-138">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




