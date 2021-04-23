---
description: Метод Unregister удаляет фильтр из реестра.
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: Метод Кбасефилтер. Unregister (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Unregister
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8b46e74e4009f6767788fa120984eca0e89fb551
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657155"
---
# <a name="cbasefilterunregister-method"></a><span data-ttu-id="43004-103">Кбасефилтер. Unregister, метод</span><span class="sxs-lookup"><span data-stu-id="43004-103">CBaseFilter.Unregister method</span></span>

<span data-ttu-id="43004-104">`Unregister`Метод удаляет фильтр из реестра.</span><span class="sxs-lookup"><span data-stu-id="43004-104">The `Unregister` method removes the filter from the registry.</span></span>

> [!Note]  
> <span data-ttu-id="43004-105">Этот метод устарел.</span><span class="sxs-lookup"><span data-stu-id="43004-105">This method is obsolete.</span></span> <span data-ttu-id="43004-106">Регистрация новых фильтров должна быть отменена с помощью функции [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="43004-106">New filters should be unregistered using the [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function.</span></span> <span data-ttu-id="43004-107">Дополнительные сведения см. [в разделе Регистрация фильтров DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="43004-107">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="43004-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43004-108">Syntax</span></span>


```C++
HRESULT Unregister();
```



## <a name="parameters"></a><span data-ttu-id="43004-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="43004-109">Parameters</span></span>

<span data-ttu-id="43004-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="43004-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43004-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43004-111">Return value</span></span>

<span data-ttu-id="43004-112">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="43004-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="43004-113">Требования</span><span class="sxs-lookup"><span data-stu-id="43004-113">Requirements</span></span>



| <span data-ttu-id="43004-114">Требование</span><span class="sxs-lookup"><span data-stu-id="43004-114">Requirement</span></span> | <span data-ttu-id="43004-115">Значение</span><span class="sxs-lookup"><span data-stu-id="43004-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43004-116">Header</span><span class="sxs-lookup"><span data-stu-id="43004-116">Header</span></span><br/>  | <dl> <span data-ttu-id="43004-117"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43004-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="43004-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43004-118">Library</span></span><br/> | <dl> <span data-ttu-id="43004-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="43004-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43004-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43004-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43004-121">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="43004-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




