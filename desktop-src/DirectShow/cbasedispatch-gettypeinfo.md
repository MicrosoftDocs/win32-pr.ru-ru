---
description: Метод GetTypeInfo извлекает сведения о типе для объекта, который затем можно использовать для получения сведений о типе для интерфейса.
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Кбаседиспатч. GetTypeInfo, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f63d79327d2f2bf2a60f06e0290aa34891e78ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657305"
---
# <a name="cbasedispatchgettypeinfo-method"></a><span data-ttu-id="dce6d-103">Кбаседиспатч. GetTypeInfo, метод</span><span class="sxs-lookup"><span data-stu-id="dce6d-103">CBaseDispatch.GetTypeInfo method</span></span>

<span data-ttu-id="dce6d-104">`GetTypeInfo`Метод получает сведения о типе для объекта, который затем можно использовать для получения сведений о типе для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="dce6d-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce6d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dce6d-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="dce6d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dce6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dce6d-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="dce6d-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="dce6d-108">Ссылка на идентификатор интерфейса (IID), указывающий интерфейс.</span><span class="sxs-lookup"><span data-stu-id="dce6d-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="dce6d-109">*итинфо*</span><span class="sxs-lookup"><span data-stu-id="dce6d-109">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="dce6d-110">Возвращаемые сведения о типе.</span><span class="sxs-lookup"><span data-stu-id="dce6d-110">Type information to return.</span></span> <span data-ttu-id="dce6d-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="dce6d-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dce6d-112">*lcid*</span><span class="sxs-lookup"><span data-stu-id="dce6d-112">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="dce6d-113">Идентификатор языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="dce6d-113">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="dce6d-114">*пптинфо*</span><span class="sxs-lookup"><span data-stu-id="dce6d-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="dce6d-115">Адрес переменной, получающей указатель **ITypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="dce6d-115">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dce6d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dce6d-116">Return value</span></span>

<span data-ttu-id="dce6d-117">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dce6d-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dce6d-118">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="dce6d-118">Possible values include the following.</span></span>



| <span data-ttu-id="dce6d-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dce6d-119">Return code</span></span>                                                                                             | <span data-ttu-id="dce6d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="dce6d-120">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="dce6d-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="dce6d-121"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="dce6d-122">Успешно.</span><span class="sxs-lookup"><span data-stu-id="dce6d-122">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="dce6d-123"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="dce6d-123"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="dce6d-124">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="dce6d-124">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="dce6d-125"><dt>**Введите \_ E \_ елементнотфаунд**</dt></span><span class="sxs-lookup"><span data-stu-id="dce6d-125"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="dce6d-126">Параметр *итинфо* не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="dce6d-126">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dce6d-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dce6d-127">Remarks</span></span>

<span data-ttu-id="dce6d-128">Этот метод ведет себя подобно методу **IDispatch:: GetTypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="dce6d-128">This method behaves like the **IDispatch::GetTypeInfo** method.</span></span> <span data-ttu-id="dce6d-129">Однако он включает дополнительный параметр *riid*, указывающий интерфейс, для которого требуется получить сведения о типе.</span><span class="sxs-lookup"><span data-stu-id="dce6d-129">However, it includes an additional parameter, *riid*, which specifies the interface for which to retrieve type information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dce6d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="dce6d-130">Requirements</span></span>



| <span data-ttu-id="dce6d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="dce6d-131">Requirement</span></span> | <span data-ttu-id="dce6d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="dce6d-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce6d-133">Header</span><span class="sxs-lookup"><span data-stu-id="dce6d-133">Header</span></span><br/>  | <dl> <span data-ttu-id="dce6d-134"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dce6d-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dce6d-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dce6d-135">Library</span></span><br/> | <dl> <span data-ttu-id="dce6d-136"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dce6d-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dce6d-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dce6d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dce6d-138">**Класс Кбаседиспатч**</span><span class="sxs-lookup"><span data-stu-id="dce6d-138">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




