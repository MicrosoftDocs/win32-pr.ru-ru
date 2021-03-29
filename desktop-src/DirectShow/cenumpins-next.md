---
description: 'Следующий метод извлекает указанное число ПИН-кодов в последовательности перечисления. Этот метод реализует метод Иенумпинс:: Next.'
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: Метод Ценумпинс. Next (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 612dcd638939b34803b7296babf7445a07cdad22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668824"
---
# <a name="cenumpinsnext-method"></a><span data-ttu-id="238be-104">Ценумпинс. Next, метод</span><span class="sxs-lookup"><span data-stu-id="238be-104">CEnumPins.Next method</span></span>

<span data-ttu-id="238be-105">Следующий метод извлекает указанное число ПИН-кодов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="238be-105">The Next method retrieves a specified number of pins in the enumeration sequence.</span></span> <span data-ttu-id="238be-106">Этот метод реализует метод [**иенумпинс:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) .</span><span class="sxs-lookup"><span data-stu-id="238be-106">This method implements the [**IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="238be-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="238be-107">Syntax</span></span>


```C++
HRESULT Next(
   ULONG cPins,
   IPin  **ppPins,
   ULONG *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="238be-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="238be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="238be-109">*кпинс*</span><span class="sxs-lookup"><span data-stu-id="238be-109">*cPins*</span></span> 
</dt> <dd>

<span data-ttu-id="238be-110">Число получаемых ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="238be-110">Number of pins to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="238be-111">*пппинс*</span><span class="sxs-lookup"><span data-stu-id="238be-111">*ppPins*</span></span> 
</dt> <dd>

<span data-ttu-id="238be-112">Массив размера *кпинс* , заполненный указателями [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="238be-112">Array of size *cPins* that is filled with [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="238be-113">*пкфетчед*</span><span class="sxs-lookup"><span data-stu-id="238be-113">*pcFetched*</span></span> 
</dt> <dd>

<span data-ttu-id="238be-114">Указатель на переменную, которая получает число полученных ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="238be-114">Pointer to a variable that receives the number of pins retrieved.</span></span> <span data-ttu-id="238be-115">Может иметь **значение NULL** , если *кпинс* равен 1.</span><span class="sxs-lookup"><span data-stu-id="238be-115">Can be **NULL** if *cPins* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="238be-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="238be-116">Return value</span></span>

<span data-ttu-id="238be-117">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="238be-117">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="238be-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="238be-118">Return code</span></span>                                                                                                | <span data-ttu-id="238be-119">Описание</span><span class="sxs-lookup"><span data-stu-id="238be-119">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="238be-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="238be-120"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="238be-121">Не удалось получить столько ПИН-кодов, сколько запрошено.</span><span class="sxs-lookup"><span data-stu-id="238be-121">Did not retrieve as many pins as requested.</span></span><br/>                                 |
| <dl> <span data-ttu-id="238be-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="238be-122"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="238be-123">Успешно.</span><span class="sxs-lookup"><span data-stu-id="238be-123">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="238be-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="238be-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="238be-125">Недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="238be-125">Invalid argument.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="238be-126"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="238be-126"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="238be-127">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="238be-127">**NULL** pointer argument.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="238be-128"><dt>**VFW \_ E \_ перечисление не \_ \_ \_ синхронизировано**</dt></span><span class="sxs-lookup"><span data-stu-id="238be-128"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="238be-129">Состояние фильтра изменилось и теперь не согласуется с перечислителем.</span><span class="sxs-lookup"><span data-stu-id="238be-129">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="238be-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="238be-130">Remarks</span></span>

<span data-ttu-id="238be-131">Этот метод извлекает указатели на указанное число ПИН-кодов, начиная с текущей позиции в перечислении и помещает их в указанный массив.</span><span class="sxs-lookup"><span data-stu-id="238be-131">This method retrieves pointers to the specified number of pins, starting at the current position in the enumeration, and places them in the specified array.</span></span>

<span data-ttu-id="238be-132">Этот метод вызывает метод [**кбасефилтер:: жетпин**](cbasefilter-getpin.md) фильтра для получения ПИН-кодов.</span><span class="sxs-lookup"><span data-stu-id="238be-132">This method calls the filter's [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method to retrieve the pins.</span></span>

<span data-ttu-id="238be-133">Если метод выполнен успешно, то все указатели **Ипин** имеют необработанные счетчики ссылок.</span><span class="sxs-lookup"><span data-stu-id="238be-133">If the method succeeds, the **IPin** pointers all have outstanding reference counts.</span></span> <span data-ttu-id="238be-134">Не забудьте освободить их по завершении.</span><span class="sxs-lookup"><span data-stu-id="238be-134">Be sure to release them when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="238be-135">Требования</span><span class="sxs-lookup"><span data-stu-id="238be-135">Requirements</span></span>



| <span data-ttu-id="238be-136">Требование</span><span class="sxs-lookup"><span data-stu-id="238be-136">Requirement</span></span> | <span data-ttu-id="238be-137">Значение</span><span class="sxs-lookup"><span data-stu-id="238be-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="238be-138">Header</span><span class="sxs-lookup"><span data-stu-id="238be-138">Header</span></span><br/>  | <dl> <span data-ttu-id="238be-139"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="238be-139"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="238be-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="238be-140">Library</span></span><br/> | <dl> <span data-ttu-id="238be-141"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="238be-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="238be-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="238be-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="238be-143">**Класс Ценумпинс**</span><span class="sxs-lookup"><span data-stu-id="238be-143">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




