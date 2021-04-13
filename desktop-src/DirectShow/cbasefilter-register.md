---
description: Метод Register добавляет фильтр в реестр.
ms.assetid: 934e421a-25a6-40fa-a48b-6d7331f34b78
title: Метод Кбасефилтер. Register (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Register
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bd7ba5a57d670ef28ffda022c95c7dc5b12df77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657824"
---
# <a name="cbasefilterregister-method"></a><span data-ttu-id="cbba9-103">Кбасефилтер. Register, метод</span><span class="sxs-lookup"><span data-stu-id="cbba9-103">CBaseFilter.Register method</span></span>

<span data-ttu-id="cbba9-104">`Register`Метод добавляет фильтр в реестр.</span><span class="sxs-lookup"><span data-stu-id="cbba9-104">The `Register` method adds the filter to the registry.</span></span>

> [!Note]  
> <span data-ttu-id="cbba9-105">Этот метод устарел.</span><span class="sxs-lookup"><span data-stu-id="cbba9-105">This method is obsolete.</span></span> <span data-ttu-id="cbba9-106">Новые фильтры должны быть зарегистрированы с помощью функции [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="cbba9-106">New filters should be registered using the [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function.</span></span> <span data-ttu-id="cbba9-107">Дополнительные сведения см. [в разделе Регистрация фильтров DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="cbba9-107">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cbba9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbba9-108">Syntax</span></span>


```C++
HRESULT Register();
```



## <a name="parameters"></a><span data-ttu-id="cbba9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbba9-109">Parameters</span></span>

<span data-ttu-id="cbba9-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cbba9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cbba9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbba9-111">Return value</span></span>

<span data-ttu-id="cbba9-112">Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="cbba9-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="cbba9-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="cbba9-113">Return code</span></span>                                                                             | <span data-ttu-id="cbba9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="cbba9-114">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="cbba9-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="cbba9-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="cbba9-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="cbba9-116">Success.</span></span><br/>                                  |
| <dl> <span data-ttu-id="cbba9-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="cbba9-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="cbba9-118">Сведения о регистрации недоступны.</span><span class="sxs-lookup"><span data-stu-id="cbba9-118">No registration information is available.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cbba9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="cbba9-119">Requirements</span></span>



| <span data-ttu-id="cbba9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="cbba9-120">Requirement</span></span> | <span data-ttu-id="cbba9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="cbba9-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbba9-122">Header</span><span class="sxs-lookup"><span data-stu-id="cbba9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="cbba9-123"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbba9-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cbba9-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cbba9-124">Library</span></span><br/> | <dl> <span data-ttu-id="cbba9-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cbba9-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbba9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbba9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbba9-127">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="cbba9-127">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




