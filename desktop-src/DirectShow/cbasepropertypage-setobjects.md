---
description: 'Метод Сетобжектс предоставляет указатели IUnknown для объектов, связанных со страницей свойств. Этот метод реализует метод Ипропертипаже:: Сетобжектс.'
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: Кбасепропертипаже. Сетобжектс, метод (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetObjects
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 197c5eb82de76fb5a5f606d8a161e853b0c1e8f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668939"
---
# <a name="cbasepropertypagesetobjects-method"></a><span data-ttu-id="4a869-104">Кбасепропертипаже. Сетобжектс, метод</span><span class="sxs-lookup"><span data-stu-id="4a869-104">CBasePropertyPage.SetObjects method</span></span>

<span data-ttu-id="4a869-105">`SetObjects`Метод предоставляет указатели **IUnknown** для объектов, связанных со страницей свойств.</span><span class="sxs-lookup"><span data-stu-id="4a869-105">The `SetObjects` method provides **IUnknown** pointers for the objects associated with the property page.</span></span> <span data-ttu-id="4a869-106">Этот метод реализует метод **ипропертипаже:: сетобжектс** .</span><span class="sxs-lookup"><span data-stu-id="4a869-106">This method implements the **IPropertyPage::SetObjects** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a869-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a869-107">Syntax</span></span>


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a><span data-ttu-id="4a869-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a869-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a869-109">*cObjects*</span><span class="sxs-lookup"><span data-stu-id="4a869-109">*cObjects*</span></span> 
</dt> <dd>

<span data-ttu-id="4a869-110">Указывает число указателей **IUnknown** в массиве, заданном параметром *ппунк*.</span><span class="sxs-lookup"><span data-stu-id="4a869-110">Specifies the number of **IUnknown** pointers in the array specified by *ppUnk*.</span></span>

</dd> <dt>

<span data-ttu-id="4a869-111">*ппунк*</span><span class="sxs-lookup"><span data-stu-id="4a869-111">*ppUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="4a869-112">Указывает массив указателей **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="4a869-112">Specifies an array of **IUnknown** pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a869-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a869-113">Return value</span></span>

<span data-ttu-id="4a869-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a869-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4a869-115">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="4a869-115">Possible values include the following.</span></span>



| <span data-ttu-id="4a869-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4a869-116">Return code</span></span>                                                                                  | <span data-ttu-id="4a869-117">Описание</span><span class="sxs-lookup"><span data-stu-id="4a869-117">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="4a869-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4a869-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4a869-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="4a869-119">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="4a869-120"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="4a869-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="4a869-121">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="4a869-121">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="4a869-122"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="4a869-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="4a869-123">Непредвиденный сбой.</span><span class="sxs-lookup"><span data-stu-id="4a869-123">Unexpected failure.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="4a869-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a869-124">Remarks</span></span>

<span data-ttu-id="4a869-125">Хотя *ппунк* указывает массив указателей **IUnknown** , класс **кбасепропертипаже** предназначен только для поддержки одного связанного объекта.</span><span class="sxs-lookup"><span data-stu-id="4a869-125">Although *ppUnk* specifies an array of **IUnknown** pointers, the **CBasePropertyPage** class is designed only to support one associated object.</span></span> <span data-ttu-id="4a869-126">Если *CObjects* больше 1, метод возвращает E \_ непредвиденные.</span><span class="sxs-lookup"><span data-stu-id="4a869-126">If *cObjects* is greater than 1, the method returns E\_UNEXPECTED.</span></span>

<span data-ttu-id="4a869-127">Если значение *CObject* равно 1, этот метод вызывает метод [**кбасепропертипаже:: OnConnect**](cbasepropertypage-onconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="4a869-127">If *cObjects* equals 1, this method calls the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method.</span></span> <span data-ttu-id="4a869-128">Если значение *CObject* равно 0, этот метод вызывает метод [**кбасепропертипаже:: ondisconnect**](cbasepropertypage-ondisconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="4a869-128">If *cObjects* equals 0, this method calls the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method.</span></span> <span data-ttu-id="4a869-129">Производный класс должен переопределять оба этих метода. Дополнительные сведения см. в комментариях к этим методам.</span><span class="sxs-lookup"><span data-stu-id="4a869-129">The derived class should override both of those methods; for details, see the remarks for those methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a869-130">Требования</span><span class="sxs-lookup"><span data-stu-id="4a869-130">Requirements</span></span>



| <span data-ttu-id="4a869-131">Требование</span><span class="sxs-lookup"><span data-stu-id="4a869-131">Requirement</span></span> | <span data-ttu-id="4a869-132">Значение</span><span class="sxs-lookup"><span data-stu-id="4a869-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a869-133">Header</span><span class="sxs-lookup"><span data-stu-id="4a869-133">Header</span></span><br/>  | <dl> <span data-ttu-id="4a869-134"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a869-134"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="4a869-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4a869-135">Library</span></span><br/> | <dl> <span data-ttu-id="4a869-136"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4a869-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a869-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a869-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a869-138">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="4a869-138">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




