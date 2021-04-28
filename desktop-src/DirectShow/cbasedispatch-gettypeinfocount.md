---
description: Кбаседиспатч. Жеттипеинфокаунт, метод Жеттипеинфокаунт извлекает количество интерфейсов сведений о типе, предоставляемых объектом.
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: Кбаседиспатч. Жеттипеинфокаунт, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81e68c94420b3d7715845f8d6bd14e26b770b44f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099892"
---
# <a name="cbasedispatchgettypeinfocount-method"></a><span data-ttu-id="954a5-103">Кбаседиспатч. Жеттипеинфокаунт, метод</span><span class="sxs-lookup"><span data-stu-id="954a5-103">CBaseDispatch.GetTypeInfoCount method</span></span>

<span data-ttu-id="954a5-104">`GetTypeInfoCount`Метод получает количество интерфейсов сведений о типе, предоставляемых объектом.</span><span class="sxs-lookup"><span data-stu-id="954a5-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="954a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="954a5-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="954a5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="954a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="954a5-107">*пктинфо*</span><span class="sxs-lookup"><span data-stu-id="954a5-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="954a5-108">Указатель на переменную, которая получает количество интерфейсов типа данных, предоставленных объектом.</span><span class="sxs-lookup"><span data-stu-id="954a5-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="954a5-109">При возврате из метода значение равно 1.</span><span class="sxs-lookup"><span data-stu-id="954a5-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="954a5-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="954a5-110">Return value</span></span>

<span data-ttu-id="954a5-111">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="954a5-111">Returns one of the following values.</span></span>



| <span data-ttu-id="954a5-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="954a5-112">Return code</span></span>                                                                               | <span data-ttu-id="954a5-113">Описание</span><span class="sxs-lookup"><span data-stu-id="954a5-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="954a5-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="954a5-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="954a5-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="954a5-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="954a5-116"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="954a5-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="954a5-117">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="954a5-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="954a5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="954a5-118">Requirements</span></span>



| <span data-ttu-id="954a5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="954a5-119">Requirement</span></span> | <span data-ttu-id="954a5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="954a5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="954a5-121">Header</span><span class="sxs-lookup"><span data-stu-id="954a5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="954a5-122"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="954a5-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="954a5-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="954a5-123">Library</span></span><br/> | <dl> <span data-ttu-id="954a5-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="954a5-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="954a5-125">См. также</span><span class="sxs-lookup"><span data-stu-id="954a5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="954a5-126">**Класс Кбаседиспатч**</span><span class="sxs-lookup"><span data-stu-id="954a5-126">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




