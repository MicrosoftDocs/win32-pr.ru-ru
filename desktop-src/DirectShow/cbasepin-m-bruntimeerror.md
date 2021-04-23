---
description: Флаг, указывающий, произошла ли ошибка во время выполнения.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: 'Элемент Кбасепин:: m_bRunTimeError (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e8b0c5548d3089a6e619f88db5e4eed19b12be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657975"
---
# <a name="cbasepinm_bruntimeerror-member"></a><span data-ttu-id="4e21e-103">Элемент Кбасепин:: m \_ брунтимиррор</span><span class="sxs-lookup"><span data-stu-id="4e21e-103">CBasePin::m\_bRunTimeError member</span></span>

<span data-ttu-id="4e21e-104">Флаг, указывающий, произошла ли ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="4e21e-104">Flag that indicates whether a run-time error has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e21e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e21e-105">Syntax</span></span>


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a><span data-ttu-id="4e21e-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="4e21e-106">Remarks</span></span>

<span data-ttu-id="4e21e-107">По умолчанию этот флаг **имеет значение false**.</span><span class="sxs-lookup"><span data-stu-id="4e21e-107">This flag defaults to **FALSE**.</span></span> <span data-ttu-id="4e21e-108">Установите для флага **значение true** , если во время потоковой передачи возникает ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="4e21e-108">Set the flag to **TRUE** if a run-time error occurs during streaming.</span></span> <span data-ttu-id="4e21e-109">Метод [**кбасепин:: Inactive**](cbasepin-inactive.md) сбрасывает флаг в **значение false**.</span><span class="sxs-lookup"><span data-stu-id="4e21e-109">The [**CBasePin::Inactive**](cbasepin-inactive.md) method resets the flag to **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e21e-110">Требования</span><span class="sxs-lookup"><span data-stu-id="4e21e-110">Requirements</span></span>



| <span data-ttu-id="4e21e-111">Требование</span><span class="sxs-lookup"><span data-stu-id="4e21e-111">Requirement</span></span> | <span data-ttu-id="4e21e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4e21e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e21e-113">Header</span><span class="sxs-lookup"><span data-stu-id="4e21e-113">Header</span></span><br/>  | <dl> <span data-ttu-id="4e21e-114"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e21e-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4e21e-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4e21e-115">Library</span></span><br/> | <dl> <span data-ttu-id="4e21e-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4e21e-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e21e-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e21e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e21e-118">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="4e21e-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




