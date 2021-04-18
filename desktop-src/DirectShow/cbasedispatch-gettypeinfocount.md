---
description: Метод Жеттипеинфокаунт извлекает количество интерфейсов сведений о типе, предоставляемых объектом.
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
ms.openlocfilehash: 39c5b78181f5f26fb5f57831345bb6345a26da85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657301"
---
# <a name="cbasedispatchgettypeinfocount-method"></a><span data-ttu-id="bd8cb-103">Кбаседиспатч. Жеттипеинфокаунт, метод</span><span class="sxs-lookup"><span data-stu-id="bd8cb-103">CBaseDispatch.GetTypeInfoCount method</span></span>

<span data-ttu-id="bd8cb-104">`GetTypeInfoCount`Метод получает количество интерфейсов сведений о типе, предоставляемых объектом.</span><span class="sxs-lookup"><span data-stu-id="bd8cb-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd8cb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd8cb-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="bd8cb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd8cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd8cb-107">*пктинфо*</span><span class="sxs-lookup"><span data-stu-id="bd8cb-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="bd8cb-108">Указатель на переменную, которая получает количество интерфейсов типа данных, предоставленных объектом.</span><span class="sxs-lookup"><span data-stu-id="bd8cb-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="bd8cb-109">При возврате из метода значение равно 1.</span><span class="sxs-lookup"><span data-stu-id="bd8cb-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd8cb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd8cb-110">Return value</span></span>

<span data-ttu-id="bd8cb-111">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bd8cb-111">Returns one of the following values.</span></span>



| <span data-ttu-id="bd8cb-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bd8cb-112">Return code</span></span>                                                                               | <span data-ttu-id="bd8cb-113">Описание</span><span class="sxs-lookup"><span data-stu-id="bd8cb-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="bd8cb-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="bd8cb-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="bd8cb-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="bd8cb-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="bd8cb-116"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="bd8cb-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="bd8cb-117">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="bd8cb-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bd8cb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="bd8cb-118">Requirements</span></span>



| <span data-ttu-id="bd8cb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="bd8cb-119">Requirement</span></span> | <span data-ttu-id="bd8cb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="bd8cb-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd8cb-121">Header</span><span class="sxs-lookup"><span data-stu-id="bd8cb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="bd8cb-122"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd8cb-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bd8cb-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bd8cb-123">Library</span></span><br/> | <dl> <span data-ttu-id="bd8cb-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="bd8cb-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd8cb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd8cb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd8cb-126">**Класс Кбаседиспатч**</span><span class="sxs-lookup"><span data-stu-id="bd8cb-126">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




