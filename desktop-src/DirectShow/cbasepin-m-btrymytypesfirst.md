---
description: Флаг, указывающий, пытается ли ПИН-код использовать собственные предпочтительные типы мультимедиа перед приемом ПИН-кода.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: 'Элемент Кбасепин:: m_bTryMyTypesFirst (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f98021b6ba97d32974f26ac4e76ca31fa54e5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669116"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a><span data-ttu-id="cdc31-103">Элемент Кбасепин:: m \_ бтримитипесфирст</span><span class="sxs-lookup"><span data-stu-id="cdc31-103">CBasePin::m\_bTryMyTypesFirst member</span></span>

<span data-ttu-id="cdc31-104">Флаг, указывающий, пытается ли ПИН-код использовать собственные предпочтительные типы мультимедиа перед приемом ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="cdc31-104">Flag that indicates whether the pin tries its own preferred media types before those of the receiving pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc31-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdc31-105">Syntax</span></span>


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a><span data-ttu-id="cdc31-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="cdc31-106">Remarks</span></span>

<span data-ttu-id="cdc31-107">По умолчанию этот флаг **имеет значение false**.</span><span class="sxs-lookup"><span data-stu-id="cdc31-107">This flag defaults to **FALSE**.</span></span> <span data-ttu-id="cdc31-108">Если флаг имеет **значение true**, метод [**Кбасепин:: агримедиатипе**](cbasepin-agreemediatype.md) меняет порядок, в котором он пытается выполнить типы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cdc31-108">If the flag is **TRUE**, the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method reverses the order in which it tries media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc31-109">Требования</span><span class="sxs-lookup"><span data-stu-id="cdc31-109">Requirements</span></span>



| <span data-ttu-id="cdc31-110">Требование</span><span class="sxs-lookup"><span data-stu-id="cdc31-110">Requirement</span></span> | <span data-ttu-id="cdc31-111">Значение</span><span class="sxs-lookup"><span data-stu-id="cdc31-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc31-112">Header</span><span class="sxs-lookup"><span data-stu-id="cdc31-112">Header</span></span><br/>  | <dl> <span data-ttu-id="cdc31-113"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdc31-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cdc31-114">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cdc31-114">Library</span></span><br/> | <dl> <span data-ttu-id="cdc31-115"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cdc31-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdc31-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdc31-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdc31-117">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="cdc31-117">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




