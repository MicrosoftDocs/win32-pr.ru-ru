---
description: Метод OnConnect предоставляет указатель IUnknown на объект, связанный со страницей свойств.
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: Метод Кбасепропертипаже. OnConnect (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38f83a7c491f1591cece8d5d85eb4525a1059d2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657962"
---
# <a name="cbasepropertypageonconnect-method"></a><span data-ttu-id="56077-103">Метод Кбасепропертипаже. OnConnect</span><span class="sxs-lookup"><span data-stu-id="56077-103">CBasePropertyPage.OnConnect method</span></span>

<span data-ttu-id="56077-104">`OnConnect`Метод предоставляет указатель **IUnknown** на объект, связанный со страницей свойств.</span><span class="sxs-lookup"><span data-stu-id="56077-104">The `OnConnect` method provides an **IUnknown** pointer to the object associated with the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="56077-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56077-105">Syntax</span></span>


```C++
virtual HRESULT OnConnect(
   IUnknown *pUnknown
);
```



## <a name="parameters"></a><span data-ttu-id="56077-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="56077-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56077-107">*pUnknown*</span><span class="sxs-lookup"><span data-stu-id="56077-107">*pUnknown*</span></span> 
</dt> <dd>

<span data-ttu-id="56077-108">Указатель на интерфейс **IUnknown** объекта.</span><span class="sxs-lookup"><span data-stu-id="56077-108">Pointer to the **IUnknown** interface of the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56077-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56077-109">Return value</span></span>

<span data-ttu-id="56077-110">Реализация базового класса возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="56077-110">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="56077-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56077-111">Remarks</span></span>

<span data-ttu-id="56077-112">Метод [**кбасепропертипаже:: сетобжектс**](cbasepropertypage-setobjects.md) вызывает `OnConnect` метод.</span><span class="sxs-lookup"><span data-stu-id="56077-112">The [**CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) method calls the `OnConnect` method.</span></span> <span data-ttu-id="56077-113">Переопределите этот метод, чтобы сохранить указатель на объект, указанный параметром *pUnknown*.</span><span class="sxs-lookup"><span data-stu-id="56077-113">Override this method to store a pointer to the object specified by *pUnknown*.</span></span> <span data-ttu-id="56077-114">Можно либо сохранить сам указатель *pUnknown* , либо запросить этот указатель для других интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="56077-114">You can either store the *pUnknown* pointer itself, or query that pointer for other interfaces.</span></span> <span data-ttu-id="56077-115">Если вы сохраняете указатель *pUnknown* , вызывайте **AddRef** перед `OnConnect` возвратом.</span><span class="sxs-lookup"><span data-stu-id="56077-115">If you store the *pUnknown* pointer, call **AddRef** before `OnConnect` returns.</span></span>

<span data-ttu-id="56077-116">В методе [**кбасепропертипаже:: OnActivate**](cbasepropertypage-onactivate.md) используйте сохраненный указатель (или указатели) для получения начальных значений для свойств диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="56077-116">In the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method, use the stored pointer (or pointers) to retrieve initial values for the dialog properties.</span></span> <span data-ttu-id="56077-117">В методе [**кбасепропертипаже:: онаппличанжес**](cbasepropertypage-onapplychanges.md) примените любые изменения к объекту.</span><span class="sxs-lookup"><span data-stu-id="56077-117">In the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method, apply any changes back to the object.</span></span> <span data-ttu-id="56077-118">Освободите все указатели в методе [**кбасепропертипаже:: ondisconnect**](cbasepropertypage-ondisconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="56077-118">Release all pointers in the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="56077-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="56077-119">Examples</span></span>


```C++
HRESULT CMyProp::OnConnect(IUnknown *pUnk)
{
    ASSERT(m_pOwningFilter == NULL);
    HRESULT hr;
    // Query pUnk for the filter's custom interface.
    hr = pUnk->QueryInterface(IID_ISomeCustomInterface,
             reinterpret_cast<void**>(&m_pOwningFilter));
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="56077-120">Требования</span><span class="sxs-lookup"><span data-stu-id="56077-120">Requirements</span></span>



| <span data-ttu-id="56077-121">Требование</span><span class="sxs-lookup"><span data-stu-id="56077-121">Requirement</span></span> | <span data-ttu-id="56077-122">Значение</span><span class="sxs-lookup"><span data-stu-id="56077-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56077-123">Header</span><span class="sxs-lookup"><span data-stu-id="56077-123">Header</span></span><br/>  | <dl> <span data-ttu-id="56077-124"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56077-124"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="56077-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="56077-125">Library</span></span><br/> | <dl> <span data-ttu-id="56077-126"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="56077-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56077-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56077-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56077-128">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="56077-128">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




