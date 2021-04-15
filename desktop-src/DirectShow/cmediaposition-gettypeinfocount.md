---
description: Метод Жеттипеинфокаунт извлекает количество интерфейсов сведений о типе, предоставляемых объектом.
ms.assetid: c98368f2-ae0c-4301-be30-7332b19f53ee
title: Кмедиапоситион. Жеттипеинфокаунт, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cac543c49b7f2f6b9dc3357bbb1c691477d9b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675771"
---
# <a name="cmediapositiongettypeinfocount-method"></a><span data-ttu-id="c8f61-103">Кмедиапоситион. Жеттипеинфокаунт, метод</span><span class="sxs-lookup"><span data-stu-id="c8f61-103">CMediaPosition.GetTypeInfoCount method</span></span>

<span data-ttu-id="c8f61-104">`GetTypeInfoCount`Метод получает количество интерфейсов сведений о типе, предоставляемых объектом.</span><span class="sxs-lookup"><span data-stu-id="c8f61-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f61-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8f61-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="c8f61-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8f61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8f61-107">*пктинфо*</span><span class="sxs-lookup"><span data-stu-id="c8f61-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c8f61-108">Указатель на переменную, которая получает количество интерфейсов типа данных, предоставленных объектом.</span><span class="sxs-lookup"><span data-stu-id="c8f61-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="c8f61-109">При возврате из метода значение равно 1.</span><span class="sxs-lookup"><span data-stu-id="c8f61-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8f61-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8f61-110">Return value</span></span>

<span data-ttu-id="c8f61-111">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c8f61-111">Returns one of the following values.</span></span>



| <span data-ttu-id="c8f61-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c8f61-112">Return code</span></span>                                                                               | <span data-ttu-id="c8f61-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c8f61-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c8f61-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c8f61-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="c8f61-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="c8f61-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="c8f61-116"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="c8f61-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="c8f61-117">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="c8f61-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c8f61-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c8f61-118">Requirements</span></span>



| <span data-ttu-id="c8f61-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c8f61-119">Requirement</span></span> | <span data-ttu-id="c8f61-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c8f61-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f61-121">Header</span><span class="sxs-lookup"><span data-stu-id="c8f61-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c8f61-122"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8f61-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c8f61-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c8f61-123">Library</span></span><br/> | <dl> <span data-ttu-id="c8f61-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c8f61-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8f61-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8f61-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f61-126">**Класс Кмедиапоситион**</span><span class="sxs-lookup"><span data-stu-id="c8f61-126">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




