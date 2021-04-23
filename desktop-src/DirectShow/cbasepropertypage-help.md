---
description: 'Метод Help вызывает справку страницы свойств. Этот метод реализует метод Ипропертипаже:: Help.'
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: Метод Кбасепропертипаже. Help (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Help
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87c8ba76928fbf0e465a8b6a3a0aaf4730759f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668990"
---
# <a name="cbasepropertypagehelp-method"></a><span data-ttu-id="a0358-104">Кбасепропертипаже. Help, метод</span><span class="sxs-lookup"><span data-stu-id="a0358-104">CBasePropertyPage.Help method</span></span>

<span data-ttu-id="a0358-105">`Help`Метод вызывает справку страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="a0358-105">The `Help` method invokes the property page help.</span></span> <span data-ttu-id="a0358-106">Этот метод реализует метод **ипропертипаже:: Help** .</span><span class="sxs-lookup"><span data-stu-id="a0358-106">This method implements the **IPropertyPage::Help** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0358-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0358-107">Syntax</span></span>


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a><span data-ttu-id="a0358-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0358-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0358-109">*лпсзелпдир*</span><span class="sxs-lookup"><span data-stu-id="a0358-109">*lpszHelpDir*</span></span> 
</dt> <dd>

<span data-ttu-id="a0358-110">Указатель на строку в ключе **хелпдир** в СВЕДЕНИЯх CLSID на странице свойств в реестре.</span><span class="sxs-lookup"><span data-stu-id="a0358-110">Pointer to the string under the **HelpDir** key in the property page's CLSID information in the registry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0358-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0358-111">Return value</span></span>

<span data-ttu-id="a0358-112">Возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="a0358-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0358-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0358-113">Remarks</span></span>

<span data-ttu-id="a0358-114">В базовом классе метод всегда возвращает E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="a0358-114">In the base class, the method always returns E\_NOTIMPL.</span></span> <span data-ttu-id="a0358-115">При сбое метода кадр вызывает **ипропертипаже:: жетпажеинфо** , чтобы получить имя файла справки и идентификатор контекста.</span><span class="sxs-lookup"><span data-stu-id="a0358-115">When the method fails, the frame calls **IPropertyPage::GetPageInfo** to get the name of the help file and context identifier.</span></span> <span data-ttu-id="a0358-116">По умолчанию они имеют **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a0358-116">By default, these are **NULL**.</span></span> <span data-ttu-id="a0358-117">Чтобы обеспечить помощь, производный класс может переопределить либо метод, `Help` либо метод [**кбасепропертипаже:: жетпажеинфо**](cbasepropertypage-getpageinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="a0358-117">To provide help, therefore, the derived class can override either the `Help` method or the [**CBasePropertyPage::GetPageInfo**](cbasepropertypage-getpageinfo.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0358-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a0358-118">Requirements</span></span>



| <span data-ttu-id="a0358-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a0358-119">Requirement</span></span> | <span data-ttu-id="a0358-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a0358-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0358-121">Header</span><span class="sxs-lookup"><span data-stu-id="a0358-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a0358-122"><dt>Кпроп. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0358-122"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="a0358-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a0358-123">Library</span></span><br/> | <dl> <span data-ttu-id="a0358-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a0358-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0358-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0358-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0358-126">**Класс Кбасепропертипаже**</span><span class="sxs-lookup"><span data-stu-id="a0358-126">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




