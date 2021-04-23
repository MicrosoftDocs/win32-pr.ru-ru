---
description: Метод GetTypeInfo извлекает сведения о типе для объекта, который затем можно использовать для получения сведений о типе для интерфейса.
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Кмедиапоситион. GetTypeInfo, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa776ca71daff67185bf9fd2c1727f9535f8ac4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669226"
---
# <a name="cmediapositiongettypeinfo-method"></a><span data-ttu-id="a34fa-103">Кмедиапоситион. GetTypeInfo, метод</span><span class="sxs-lookup"><span data-stu-id="a34fa-103">CMediaPosition.GetTypeInfo method</span></span>

<span data-ttu-id="a34fa-104">`GetTypeInfo`Метод получает сведения о типе для объекта, который затем можно использовать для получения сведений о типе для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a34fa-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a34fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a34fa-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="a34fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a34fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a34fa-107">*итинфо*</span><span class="sxs-lookup"><span data-stu-id="a34fa-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="a34fa-108">Возвращаемые сведения о типе.</span><span class="sxs-lookup"><span data-stu-id="a34fa-108">Type information to return.</span></span> <span data-ttu-id="a34fa-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a34fa-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a34fa-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="a34fa-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="a34fa-111">Идентификатор языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="a34fa-111">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a34fa-112">*пптинфо*</span><span class="sxs-lookup"><span data-stu-id="a34fa-112">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="a34fa-113">Адрес переменной, получающей указатель **ITypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="a34fa-113">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a34fa-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a34fa-114">Return value</span></span>

<span data-ttu-id="a34fa-115">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a34fa-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a34fa-116">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="a34fa-116">Possible values include the following.</span></span>



| <span data-ttu-id="a34fa-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a34fa-117">Return code</span></span>                                                                                             | <span data-ttu-id="a34fa-118">Описание</span><span class="sxs-lookup"><span data-stu-id="a34fa-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="a34fa-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a34fa-119"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="a34fa-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="a34fa-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="a34fa-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="a34fa-121"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="a34fa-122">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="a34fa-122">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="a34fa-123"><dt>**Введите \_ E \_ елементнотфаунд**</dt></span><span class="sxs-lookup"><span data-stu-id="a34fa-123"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="a34fa-124">Параметр *итинфо* не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="a34fa-124">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a34fa-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a34fa-125">Requirements</span></span>



| <span data-ttu-id="a34fa-126">Требование</span><span class="sxs-lookup"><span data-stu-id="a34fa-126">Requirement</span></span> | <span data-ttu-id="a34fa-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a34fa-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a34fa-128">Header</span><span class="sxs-lookup"><span data-stu-id="a34fa-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a34fa-129"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a34fa-129"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a34fa-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a34fa-130">Library</span></span><br/> | <dl> <span data-ttu-id="a34fa-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="a34fa-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a34fa-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a34fa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a34fa-133">**Класс Кмедиапоситион**</span><span class="sxs-lookup"><span data-stu-id="a34fa-133">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




