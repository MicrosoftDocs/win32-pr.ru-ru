---
description: 'Метод Куеридиректион извлекает направление ПИН-кода (ввод или вывод). Этот метод реализует метод Ипин:: Куеридиректион.'
ms.assetid: c28332dc-5ac4-4c89-98b4-281424f36ba9
title: Кбасепин. Куеридиректион, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryDirection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e2ebfaa3d12b5f582b4b67014280fa0a0d5299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668545"
---
# <a name="cbasepinquerydirection-method"></a><span data-ttu-id="54fa1-104">Кбасепин. Куеридиректион, метод</span><span class="sxs-lookup"><span data-stu-id="54fa1-104">CBasePin.QueryDirection method</span></span>

<span data-ttu-id="54fa1-105">`QueryDirection`Метод получает направление ПИН-кода (ввод или вывод).</span><span class="sxs-lookup"><span data-stu-id="54fa1-105">The `QueryDirection` method retrieves the direction of the pin (input or output).</span></span> <span data-ttu-id="54fa1-106">Этот метод реализует метод [**Ипин:: куеридиректион**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) .</span><span class="sxs-lookup"><span data-stu-id="54fa1-106">This method implements the [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="54fa1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54fa1-107">Syntax</span></span>


```C++
HRESULT QueryDirection(
   PIN_DIRECTION *pPinDir
);
```



## <a name="parameters"></a><span data-ttu-id="54fa1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="54fa1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54fa1-109">*ппиндир*</span><span class="sxs-lookup"><span data-stu-id="54fa1-109">*pPinDir*</span></span> 
</dt> <dd>

<span data-ttu-id="54fa1-110">Указатель на переменную, которая получает элемент перечисляемого [**типа \_ направления**](/windows/win32/api/strmif/ne-strmif-pin_direction) .</span><span class="sxs-lookup"><span data-stu-id="54fa1-110">Pointer to a variable that receives a member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54fa1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54fa1-111">Return value</span></span>

<span data-ttu-id="54fa1-112">Возвращает значение S \_ (ОК) или \_ указатель E.</span><span class="sxs-lookup"><span data-stu-id="54fa1-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="54fa1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="54fa1-113">Requirements</span></span>



| <span data-ttu-id="54fa1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="54fa1-114">Requirement</span></span> | <span data-ttu-id="54fa1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="54fa1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54fa1-116">Header</span><span class="sxs-lookup"><span data-stu-id="54fa1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="54fa1-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54fa1-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="54fa1-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="54fa1-118">Library</span></span><br/> | <dl> <span data-ttu-id="54fa1-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="54fa1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54fa1-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54fa1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54fa1-121">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="54fa1-121">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




