---
description: 'Метод Енумпинс перечисляет контакты в этом фильтре. Этот метод реализует метод Ибасефилтер:: Енумпинс.'
ms.assetid: c1015ed3-658f-4f96-a1fb-e04b81a9ddb5
title: Кбасефилтер. Енумпинс, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.EnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66a0f88a9749ba1dabb982e2f275da8a4be2a422
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657685"
---
# <a name="cbasefilterenumpins-method"></a><span data-ttu-id="bdd9b-104">Кбасефилтер. Енумпинс, метод</span><span class="sxs-lookup"><span data-stu-id="bdd9b-104">CBaseFilter.EnumPins method</span></span>

<span data-ttu-id="bdd9b-105">`EnumPins`Метод перечисляет ПИН-коды в этом фильтре.</span><span class="sxs-lookup"><span data-stu-id="bdd9b-105">The `EnumPins` method enumerates the pins on this filter.</span></span> <span data-ttu-id="bdd9b-106">Этот метод реализует метод [**ибасефилтер:: енумпинс**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) .</span><span class="sxs-lookup"><span data-stu-id="bdd9b-106">This method implements the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd9b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bdd9b-107">Syntax</span></span>


```C++
HRESULT EnumPins(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="bdd9b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bdd9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdd9b-109">*ппенум*</span><span class="sxs-lookup"><span data-stu-id="bdd9b-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="bdd9b-110">Адрес переменной, которая получает указатель на интерфейс [**иенумпинс**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="bdd9b-110">Address of a variable that receives a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdd9b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bdd9b-111">Return value</span></span>

<span data-ttu-id="bdd9b-112">Возвращает одно из следующих значений **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bdd9b-112">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="bdd9b-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bdd9b-113">Return code</span></span>                                                                                   | <span data-ttu-id="bdd9b-114">Описание</span><span class="sxs-lookup"><span data-stu-id="bdd9b-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="bdd9b-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="bdd9b-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bdd9b-116">Успешно</span><span class="sxs-lookup"><span data-stu-id="bdd9b-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="bdd9b-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bdd9b-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bdd9b-118">Недостаточно памяти</span><span class="sxs-lookup"><span data-stu-id="bdd9b-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="bdd9b-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="bdd9b-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bdd9b-120">**Пустой** аргумент указателя</span><span class="sxs-lookup"><span data-stu-id="bdd9b-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bdd9b-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bdd9b-121">Remarks</span></span>

<span data-ttu-id="bdd9b-122">Этот метод создает экземпляр базового класса [**ценумпинс**](cenumpins.md) и возвращает указатель на этот объект типа **иенумпинс**.</span><span class="sxs-lookup"><span data-stu-id="bdd9b-122">This method creates an instance of the [**CEnumPins**](cenumpins.md) base class, and returns a pointer to that object, of type **IEnumPins**.</span></span> <span data-ttu-id="bdd9b-123">Класс **ценумпинс** вызывает метод [**Кбасефилтер:: жетпин**](cbasefilter-getpin.md) фильтра для перечисления ПИН-кодов в фильтре.</span><span class="sxs-lookup"><span data-stu-id="bdd9b-123">The **CEnumPins** class calls the filter's [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method to enumerate the pins on the filter.</span></span>

<span data-ttu-id="bdd9b-124">Если этот метод завершился успешно, то интерфейс **иенумпинс** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="bdd9b-124">If this method succeeds, the **IEnumPins** interface has an outstanding reference count.</span></span> <span data-ttu-id="bdd9b-125">Вызывающий объект должен освободить интерфейс.</span><span class="sxs-lookup"><span data-stu-id="bdd9b-125">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdd9b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="bdd9b-126">Requirements</span></span>



| <span data-ttu-id="bdd9b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="bdd9b-127">Requirement</span></span> | <span data-ttu-id="bdd9b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="bdd9b-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd9b-129">Header</span><span class="sxs-lookup"><span data-stu-id="bdd9b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bdd9b-130"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdd9b-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bdd9b-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bdd9b-131">Library</span></span><br/> | <dl> <span data-ttu-id="bdd9b-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bdd9b-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdd9b-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bdd9b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdd9b-134">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="bdd9b-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




