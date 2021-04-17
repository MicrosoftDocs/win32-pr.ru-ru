---
description: Метод ondisconnect вызывается, когда страница свойств должна освободить связанный объект.
ms.assetid: 55bab0ca-587e-405c-9025-f391cf08a620
title: Метод Кбасепропертипаже. ondisconnect (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDisconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd251d20ca82ad0374a613d9ee73f0eaee21d31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665250"
---
# <a name="cbasepropertypageondisconnect-method"></a><span data-ttu-id="a40e3-103">Кбасепропертипаже. ondisconnect, метод</span><span class="sxs-lookup"><span data-stu-id="a40e3-103">CBasePropertyPage.OnDisconnect method</span></span>

<span data-ttu-id="a40e3-104">`OnDisconnect`Метод вызывается, когда страница свойств должна освободить связанный объект.</span><span class="sxs-lookup"><span data-stu-id="a40e3-104">The `OnDisconnect` method is called when the property page should release the associated object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a40e3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a40e3-105">Syntax</span></span>


```C++
virtual HRESULT OnDisconnect();
```



## <a name="parameters"></a><span data-ttu-id="a40e3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a40e3-106">Parameters</span></span>

<span data-ttu-id="a40e3-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a40e3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a40e3-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a40e3-108">Return value</span></span>

<span data-ttu-id="a40e3-109">Реализация базового класса возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a40e3-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a40e3-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a40e3-110">Remarks</span></span>

<span data-ttu-id="a40e3-111">Метод [**кбасепропертипаже:: сетобжектс**](cbasepropertypage-setobjects.md) вызывает `OnDisconnect` метод.</span><span class="sxs-lookup"><span data-stu-id="a40e3-111">The [**CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) method calls the `OnDisconnect` method.</span></span> <span data-ttu-id="a40e3-112">Переопределите, `OnDisconnect` чтобы освободить все указатели, полученные в методе [**кбасепропертипаже:: OnConnect**](cbasepropertypage-onconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="a40e3-112">Override `OnDisconnect` to release any pointers that were obtained in the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="a40e3-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="a40e3-113">Examples</span></span>


```C++
HRESULT CMyProp::OnDisconnect(void)
{
    if (m_pOwningFilter)
    {
        m_pOwningFilter->Release();
        m_pOwningFilter = NULL;
    }
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="a40e3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a40e3-114">Requirements</span></span>



| <span data-ttu-id="a40e3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a40e3-115">Requirement</span></span> | <span data-ttu-id="a40e3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a40e3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a40e3-117">Header</span><span class="sxs-lookup"><span data-stu-id="a40e3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a40e3-118"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a40e3-118"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="a40e3-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a40e3-119">Library</span></span><br/> | <dl> <span data-ttu-id="a40e3-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a40e3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a40e3-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a40e3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a40e3-122">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="a40e3-122">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




