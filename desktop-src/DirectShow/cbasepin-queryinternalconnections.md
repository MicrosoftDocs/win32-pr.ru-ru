---
description: 'Метод Куеринтерналконнектионс извлекает контакты, которые подключены внутренне к этому ПИН-коду (в рамках фильтра). Этот метод реализует метод Ипин:: Куеринтерналконнектионс.'
ms.assetid: 08344fc5-38b2-4dbe-8ef9-30d2fcd64187
title: Кбасепин. Куеринтерналконнектионс, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryInternalConnections
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99a636295fc87347a1735ab028b6de342e887d55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657339"
---
# <a name="cbasepinqueryinternalconnections-method"></a><span data-ttu-id="1f945-104">Кбасепин. Куеринтерналконнектионс, метод</span><span class="sxs-lookup"><span data-stu-id="1f945-104">CBasePin.QueryInternalConnections method</span></span>

<span data-ttu-id="1f945-105">`QueryInternalConnections`Метод получает контакты, которые подключены внутренне к этому ПИН-коду (в рамках фильтра).</span><span class="sxs-lookup"><span data-stu-id="1f945-105">The `QueryInternalConnections` method retrieves the pins that are connected internally to this pin (within the filter).</span></span> <span data-ttu-id="1f945-106">Этот метод реализует метод [**Ипин:: куеринтерналконнектионс**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) .</span><span class="sxs-lookup"><span data-stu-id="1f945-106">This method implements the [**IPin::QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f945-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f945-107">Syntax</span></span>


```C++
HRESULT QueryInternalConnections(
   IPin  *apPin,
   ULONG *nPin
);
```



## <a name="parameters"></a><span data-ttu-id="1f945-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f945-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f945-109">*Списке*</span><span class="sxs-lookup"><span data-stu-id="1f945-109">*apPin*</span></span> 
</dt> <dd>

<span data-ttu-id="1f945-110">Адрес массива указателей [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="1f945-110">Address of an array of [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="1f945-111">*нпин*</span><span class="sxs-lookup"><span data-stu-id="1f945-111">*nPin*</span></span> 
</dt> <dd>

<span data-ttu-id="1f945-112">В поле входные данные задает размер массива.</span><span class="sxs-lookup"><span data-stu-id="1f945-112">On input, specifies the size of the array.</span></span> <span data-ttu-id="1f945-113">Когда метод возвращает значение, ему присваивается число указателей, возвращаемых в массиве.</span><span class="sxs-lookup"><span data-stu-id="1f945-113">When the method returns, the value is set to the number of pointers returned in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f945-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f945-114">Return value</span></span>

<span data-ttu-id="1f945-115">Возвращает одно из значений **HRESULT** , приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1f945-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="1f945-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1f945-116">Return code</span></span>                                                                               | <span data-ttu-id="1f945-117">Описание</span><span class="sxs-lookup"><span data-stu-id="1f945-117">Description</span></span>                         |
|-------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="1f945-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1f945-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="1f945-119">Недостаточный размер массива.</span><span class="sxs-lookup"><span data-stu-id="1f945-119">Insufficient array size.</span></span><br/> |
| <dl> <span data-ttu-id="1f945-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1f945-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="1f945-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="1f945-121">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="1f945-122"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="1f945-122"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="1f945-123">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="1f945-123">Failure.</span></span><br/>                 |
| <dl> <span data-ttu-id="1f945-124"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="1f945-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="1f945-125">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="1f945-125">Not implemented.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="1f945-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f945-126">Remarks</span></span>

<span data-ttu-id="1f945-127">В некоторых фильтрах входные ПИН-коды соответствуют определенным выходным закреплениям.</span><span class="sxs-lookup"><span data-stu-id="1f945-127">On some filters, input pins correspond to particular output pins.</span></span> <span data-ttu-id="1f945-128">Для каждого ПИН-кода этот метод заполняет массив указателями на соответствующие сигналы.</span><span class="sxs-lookup"><span data-stu-id="1f945-128">For each pin, this method fills an array with pointers to the corresponding pins.</span></span> <span data-ttu-id="1f945-129">Если каждый входной ПИН-код предоставляет данные для каждого выходного контакта, возвращается E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="1f945-129">If every input pin provides data for every output pin, return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f945-130">Требования</span><span class="sxs-lookup"><span data-stu-id="1f945-130">Requirements</span></span>



| <span data-ttu-id="1f945-131">Требование</span><span class="sxs-lookup"><span data-stu-id="1f945-131">Requirement</span></span> | <span data-ttu-id="1f945-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1f945-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f945-133">Header</span><span class="sxs-lookup"><span data-stu-id="1f945-133">Header</span></span><br/>  | <dl> <span data-ttu-id="1f945-134"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f945-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1f945-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1f945-135">Library</span></span><br/> | <dl> <span data-ttu-id="1f945-136"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1f945-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f945-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f945-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f945-138">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="1f945-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




