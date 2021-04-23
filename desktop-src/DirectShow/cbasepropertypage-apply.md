---
description: 'Метод Apply применяет текущие значения страницы свойств к объекту, связанному со страницей свойств. Этот метод реализует метод Ипропертипаже:: Apply.'
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: Метод Кбасепропертипаже. Apply (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21d1208979cca167b059cb720c492ac51c362c39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657490"
---
# <a name="cbasepropertypageapply-method"></a><span data-ttu-id="1ff0c-104">Кбасепропертипаже. Apply, метод</span><span class="sxs-lookup"><span data-stu-id="1ff0c-104">CBasePropertyPage.Apply method</span></span>

<span data-ttu-id="1ff0c-105">`Apply`Метод применяет текущие значения страницы свойств к объекту, связанному со страницей свойств.</span><span class="sxs-lookup"><span data-stu-id="1ff0c-105">The `Apply` method applies the current property page values to the object associated with the property page.</span></span> <span data-ttu-id="1ff0c-106">Этот метод реализует метод **ипропертипаже:: Apply** .</span><span class="sxs-lookup"><span data-stu-id="1ff0c-106">This method implements the **IPropertyPage::Apply** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff0c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ff0c-107">Syntax</span></span>


```C++
HRESULT Apply();
```



## <a name="parameters"></a><span data-ttu-id="1ff0c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ff0c-108">Parameters</span></span>

<span data-ttu-id="1ff0c-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1ff0c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1ff0c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ff0c-110">Return value</span></span>

<span data-ttu-id="1ff0c-111">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1ff0c-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1ff0c-112">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="1ff0c-112">Possible values include the following.</span></span>



| <span data-ttu-id="1ff0c-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1ff0c-113">Return code</span></span>                                                                                  | <span data-ttu-id="1ff0c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="1ff0c-114">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="1ff0c-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1ff0c-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1ff0c-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="1ff0c-116">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="1ff0c-117"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="1ff0c-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="1ff0c-118">Непредвиденный сбой.</span><span class="sxs-lookup"><span data-stu-id="1ff0c-118">Unexpected failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1ff0c-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ff0c-119">Remarks</span></span>

<span data-ttu-id="1ff0c-120">Если флаг [**\_ бдирти кбасепропертипаже:: m**](cbasepropertypage-m-bdirty.md) имеет **значение true**, этот метод вызывает метод [**кбасепропертипаже:: онаппличанжес**](cbasepropertypage-onapplychanges.md) .</span><span class="sxs-lookup"><span data-stu-id="1ff0c-120">If the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag is **TRUE**, this method calls the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method.</span></span> <span data-ttu-id="1ff0c-121">Переопределите **онаппличанжес** , чтобы применить изменения к объекту.</span><span class="sxs-lookup"><span data-stu-id="1ff0c-121">Override **OnApplyChanges** to apply the changes to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff0c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1ff0c-122">Requirements</span></span>



| <span data-ttu-id="1ff0c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1ff0c-123">Requirement</span></span> | <span data-ttu-id="1ff0c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1ff0c-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff0c-125">Header</span><span class="sxs-lookup"><span data-stu-id="1ff0c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1ff0c-126"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ff0c-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="1ff0c-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1ff0c-127">Library</span></span><br/> | <dl> <span data-ttu-id="1ff0c-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1ff0c-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ff0c-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ff0c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ff0c-130">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="1ff0c-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




