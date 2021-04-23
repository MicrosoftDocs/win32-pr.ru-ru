---
description: 'Метод Испажедирти указывает, изменилась ли страница свойств с момента ее активации или последнего вызова метода Ипропертипаже:: Apply. Этот метод реализует метод Ипропертипаже:: Испажедирти.'
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Кбасепропертипаже. Испажедирти, метод (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.IsPageDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c69c2e7d480f63542e146c73e56b9e692693f665
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657714"
---
# <a name="cbasepropertypageispagedirty-method"></a><span data-ttu-id="65f7d-104">Кбасепропертипаже. Испажедирти, метод</span><span class="sxs-lookup"><span data-stu-id="65f7d-104">CBasePropertyPage.IsPageDirty method</span></span>

<span data-ttu-id="65f7d-105">`IsPageDirty`Метод указывает, изменилась ли страница свойств с момента ее активации или последнего вызова метода **ипропертипаже:: Apply**.</span><span class="sxs-lookup"><span data-stu-id="65f7d-105">The `IsPageDirty` method indicates whether the property page has changed since it was activated or since the most recent call to **IPropertyPage::Apply**.</span></span> <span data-ttu-id="65f7d-106">Этот метод реализует метод **ипропертипаже:: испажедирти** .</span><span class="sxs-lookup"><span data-stu-id="65f7d-106">This method implements the **IPropertyPage::IsPageDirty** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f7d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65f7d-107">Syntax</span></span>


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a><span data-ttu-id="65f7d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="65f7d-108">Parameters</span></span>

<span data-ttu-id="65f7d-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="65f7d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="65f7d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65f7d-110">Return value</span></span>

<span data-ttu-id="65f7d-111">Возвращает значение S \_ ОК, если [**кбасепропертипаже:: m \_ Бдирти**](cbasepropertypage-m-bdirty.md) имеет **значение true**, или \_ false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="65f7d-111">Returns S\_OK if [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) is **TRUE**, or S\_FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="65f7d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="65f7d-112">Requirements</span></span>



| <span data-ttu-id="65f7d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="65f7d-113">Requirement</span></span> | <span data-ttu-id="65f7d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="65f7d-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65f7d-115">Header</span><span class="sxs-lookup"><span data-stu-id="65f7d-115">Header</span></span><br/>  | <dl> <span data-ttu-id="65f7d-116"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65f7d-116"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="65f7d-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="65f7d-117">Library</span></span><br/> | <dl> <span data-ttu-id="65f7d-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="65f7d-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65f7d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65f7d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65f7d-120">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="65f7d-120">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




