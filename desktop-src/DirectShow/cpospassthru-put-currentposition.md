---
description: Метод размещения \_ CurrentPosition задает текущую точку относительно общей продолжительности потока. Этот метод реализует метод Имедиапоситион::p UT \_ CurrentPosition.
ms.assetid: 22d7e9e4-47da-45b5-9be0-3c5128f90353
title: Метод CPosPassThru.put_CurrentPosition (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85426636a34d0e197b36496d5a38a847c61b9501
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679964"
---
# <a name="cpospassthruput_currentposition-method"></a><span data-ttu-id="ed686-104">Кпоспасссру. размещение \_ метода CurrentPosition</span><span class="sxs-lookup"><span data-stu-id="ed686-104">CPosPassThru.put\_CurrentPosition method</span></span>

<span data-ttu-id="ed686-105">`put_CurrentPosition`Метод задает текущую точку относительно общей продолжительности потока.</span><span class="sxs-lookup"><span data-stu-id="ed686-105">The `put_CurrentPosition` method sets the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="ed686-106">Этот метод реализует метод [**имедиапоситион::p UT \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) .</span><span class="sxs-lookup"><span data-stu-id="ed686-106">This method implements the [**IMediaPosition::put\_CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed686-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed686-107">Syntax</span></span>


```C++
HRESULT put_CurrentPosition(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="ed686-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed686-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed686-109">*ллтиме*</span><span class="sxs-lookup"><span data-stu-id="ed686-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="ed686-110">Новое расположение в секундах.</span><span class="sxs-lookup"><span data-stu-id="ed686-110">New position, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed686-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed686-111">Return value</span></span>

<span data-ttu-id="ed686-112">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="ed686-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed686-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ed686-113">Requirements</span></span>



| <span data-ttu-id="ed686-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ed686-114">Requirement</span></span> | <span data-ttu-id="ed686-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ed686-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed686-116">Header</span><span class="sxs-lookup"><span data-stu-id="ed686-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ed686-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed686-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ed686-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ed686-118">Library</span></span><br/> | <dl> <span data-ttu-id="ed686-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ed686-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed686-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed686-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed686-121">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="ed686-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




