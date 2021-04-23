---
description: Метод Онаппличанжес вызывается, когда пользователь применяет изменения к странице свойств.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: Кбасепропертипаже. Онаппличанжес, метод (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnApplyChanges
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbcea308a8daaa8b9fdf15be765dc5d3a0df182c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669283"
---
# <a name="cbasepropertypageonapplychanges-method"></a><span data-ttu-id="15d76-103">Кбасепропертипаже. Онаппличанжес, метод</span><span class="sxs-lookup"><span data-stu-id="15d76-103">CBasePropertyPage.OnApplyChanges method</span></span>

<span data-ttu-id="15d76-104">`OnApplyChanges`Метод вызывается, когда пользователь применяет изменения к странице свойств.</span><span class="sxs-lookup"><span data-stu-id="15d76-104">The `OnApplyChanges` method is called when the user applies changes to the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="15d76-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15d76-105">Syntax</span></span>


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a><span data-ttu-id="15d76-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="15d76-106">Parameters</span></span>

<span data-ttu-id="15d76-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="15d76-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15d76-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15d76-108">Return value</span></span>

<span data-ttu-id="15d76-109">Реализация базового класса возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="15d76-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="15d76-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15d76-110">Remarks</span></span>

<span data-ttu-id="15d76-111">Метод [**кбасепропертипаже:: Apply**](cbasepropertypage-apply.md) вызывает, `OnApplyChanges` Если флаг [**кбасепропертипаже:: m \_ бдирти**](cbasepropertypage-m-bdirty.md) имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="15d76-111">The [**CBasePropertyPage::Apply**](cbasepropertypage-apply.md) method calls `OnApplyChanges` if the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag is **TRUE**.</span></span> <span data-ttu-id="15d76-112">Переопределите `OnApplyChanges` для обработки изменений и сбросьте **m \_ Бдирти** в **значение false**.</span><span class="sxs-lookup"><span data-stu-id="15d76-112">Override `OnApplyChanges` to process the changes and reset **m\_bDirty** to **FALSE**.</span></span>

## <a name="examples"></a><span data-ttu-id="15d76-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="15d76-113">Examples</span></span>


```C++
HRESULT CMyProp::OnApplyChanges(void)
{
    ASSERT(m_pOwningFilter != NULL);
    return m_pOwningFilter->SetSomeProperty(&m_lNewVal);
}
```



## <a name="requirements"></a><span data-ttu-id="15d76-114">Требования</span><span class="sxs-lookup"><span data-stu-id="15d76-114">Requirements</span></span>



| <span data-ttu-id="15d76-115">Требование</span><span class="sxs-lookup"><span data-stu-id="15d76-115">Requirement</span></span> | <span data-ttu-id="15d76-116">Значение</span><span class="sxs-lookup"><span data-stu-id="15d76-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15d76-117">Header</span><span class="sxs-lookup"><span data-stu-id="15d76-117">Header</span></span><br/>  | <dl> <span data-ttu-id="15d76-118"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15d76-118"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="15d76-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="15d76-119">Library</span></span><br/> | <dl> <span data-ttu-id="15d76-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="15d76-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15d76-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15d76-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d76-122">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="15d76-122">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




