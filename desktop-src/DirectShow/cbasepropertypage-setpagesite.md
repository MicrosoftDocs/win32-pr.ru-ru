---
description: 'Метод Сетпажесите инициализирует страницу свойств и предоставляет указатель на интерфейс Ипропертипажесите рамки свойства. Этот метод реализует метод Ипропертипаже:: Сетпажесите.'
ms.assetid: 16c4633f-2f91-4b1b-a47c-4ef945c3af00
title: Кбасепропертипаже. Сетпажесите, метод (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetPageSite
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a165ff60971cef3d2373e0f07b2abee554308279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656970"
---
# <a name="cbasepropertypagesetpagesite-method"></a><span data-ttu-id="1765c-104">Кбасепропертипаже. Сетпажесите, метод</span><span class="sxs-lookup"><span data-stu-id="1765c-104">CBasePropertyPage.SetPageSite method</span></span>

<span data-ttu-id="1765c-105">`SetPageSite`Метод инициализирует страницу свойств и предоставляет указатель на интерфейс **ипропертипажесите** рамки свойства.</span><span class="sxs-lookup"><span data-stu-id="1765c-105">The `SetPageSite` method initializes the property page and provides a pointer to the property frame's **IPropertyPageSite** interface.</span></span> <span data-ttu-id="1765c-106">Этот метод реализует метод **ипропертипаже:: сетпажесите** .</span><span class="sxs-lookup"><span data-stu-id="1765c-106">This method implements the **IPropertyPage::SetPageSite** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1765c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1765c-107">Syntax</span></span>


```C++
HRESULT SetPageSite(
   IPropertyPageSite *pPageSite
);
```



## <a name="parameters"></a><span data-ttu-id="1765c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1765c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1765c-109">*ппажесите*</span><span class="sxs-lookup"><span data-stu-id="1765c-109">*pPageSite*</span></span> 
</dt> <dd>

<span data-ttu-id="1765c-110">Указатель на интерфейс **ипропертипажесите** .</span><span class="sxs-lookup"><span data-stu-id="1765c-110">Pointer to the **IPropertyPageSite** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1765c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1765c-111">Return value</span></span>

<span data-ttu-id="1765c-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1765c-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1765c-113">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="1765c-113">Possible values include the following.</span></span>



| <span data-ttu-id="1765c-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1765c-114">Return code</span></span>                                                                                  | <span data-ttu-id="1765c-115">Описание</span><span class="sxs-lookup"><span data-stu-id="1765c-115">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="1765c-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1765c-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1765c-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="1765c-117">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="1765c-118"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="1765c-118"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="1765c-119">Непредвиденный сбой.</span><span class="sxs-lookup"><span data-stu-id="1765c-119">Unexpected failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1765c-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1765c-120">Remarks</span></span>

<span data-ttu-id="1765c-121">Метод сохраняет указатель *ппажесите* в переменной члена [**кбасепропертипаже:: m \_ ппажесите**](cbasepropertypage-m-ppagesite.md) .</span><span class="sxs-lookup"><span data-stu-id="1765c-121">The method stores the *pPageSite* pointer in the [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="1765c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1765c-122">Requirements</span></span>



| <span data-ttu-id="1765c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1765c-123">Requirement</span></span> | <span data-ttu-id="1765c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1765c-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1765c-125">Header</span><span class="sxs-lookup"><span data-stu-id="1765c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1765c-126"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1765c-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="1765c-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1765c-127">Library</span></span><br/> | <dl> <span data-ttu-id="1765c-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1765c-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1765c-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1765c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1765c-130">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="1765c-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




