---
description: Метод Самплепропс извлекает свойства последнего примера в \_ \_ структуре свойств SAMPLE2.
ms.assetid: d4c98c35-f8b2-4111-bae9-4e0f58a0cc8a
title: Кбасеинпутпин. Самплепропс, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.SampleProps
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45663cfd221c7a31abe5f85a494869b24d1ddd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658024"
---
# <a name="cbaseinputpinsampleprops-method"></a><span data-ttu-id="39d2d-103">Кбасеинпутпин. Самплепропс, метод</span><span class="sxs-lookup"><span data-stu-id="39d2d-103">CBaseInputPin.SampleProps method</span></span>

<span data-ttu-id="39d2d-104">`SampleProps`Метод получает свойства последнего примера в структуре [**\_ \_ свойств SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="39d2d-104">The `SampleProps` method retrieves the properties of the most recent sample, in an [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d2d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39d2d-105">Syntax</span></span>


```C++
AM_SAMPLE2_PROPERTIES* SampleProps();
```



## <a name="parameters"></a><span data-ttu-id="39d2d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39d2d-106">Parameters</span></span>

<span data-ttu-id="39d2d-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="39d2d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39d2d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39d2d-108">Return value</span></span>

<span data-ttu-id="39d2d-109">Возвращает адрес переменной члена [**кбасеинпутпин:: m \_ самплепропс**](cbaseinputpin-m-sampleprops.md) .</span><span class="sxs-lookup"><span data-stu-id="39d2d-109">Returns the address of the [**CBaseInputPin::m\_SampleProps**](cbaseinputpin-m-sampleprops.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="39d2d-110">Требования</span><span class="sxs-lookup"><span data-stu-id="39d2d-110">Requirements</span></span>



| <span data-ttu-id="39d2d-111">Требование</span><span class="sxs-lookup"><span data-stu-id="39d2d-111">Requirement</span></span> | <span data-ttu-id="39d2d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="39d2d-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39d2d-113">Header</span><span class="sxs-lookup"><span data-stu-id="39d2d-113">Header</span></span><br/>  | <dl> <span data-ttu-id="39d2d-114"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39d2d-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="39d2d-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="39d2d-115">Library</span></span><br/> | <dl> <span data-ttu-id="39d2d-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="39d2d-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39d2d-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39d2d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d2d-118">**Класс Кбасеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="39d2d-118">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




