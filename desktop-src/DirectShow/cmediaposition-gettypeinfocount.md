---
description: Кмедиапоситион. Жеттипеинфокаунт, метод Жеттипеинфокаунт извлекает количество интерфейсов сведений о типе, предоставляемых объектом.
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
ms.openlocfilehash: 8cfc54f414a6722f7f69a0330fad2d1a0cfab425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095482"
---
# <a name="cmediapositiongettypeinfocount-method"></a><span data-ttu-id="f2b94-103">Кмедиапоситион. Жеттипеинфокаунт, метод</span><span class="sxs-lookup"><span data-stu-id="f2b94-103">CMediaPosition.GetTypeInfoCount method</span></span>

<span data-ttu-id="f2b94-104">`GetTypeInfoCount`Метод получает количество интерфейсов сведений о типе, предоставляемых объектом.</span><span class="sxs-lookup"><span data-stu-id="f2b94-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2b94-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2b94-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="f2b94-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2b94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2b94-107">*пктинфо*</span><span class="sxs-lookup"><span data-stu-id="f2b94-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="f2b94-108">Указатель на переменную, которая получает количество интерфейсов типа данных, предоставленных объектом.</span><span class="sxs-lookup"><span data-stu-id="f2b94-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="f2b94-109">При возврате из метода значение равно 1.</span><span class="sxs-lookup"><span data-stu-id="f2b94-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2b94-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2b94-110">Return value</span></span>

<span data-ttu-id="f2b94-111">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f2b94-111">Returns one of the following values.</span></span>



| <span data-ttu-id="f2b94-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f2b94-112">Return code</span></span>                                                                               | <span data-ttu-id="f2b94-113">Описание</span><span class="sxs-lookup"><span data-stu-id="f2b94-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f2b94-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f2b94-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="f2b94-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="f2b94-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="f2b94-116"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="f2b94-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="f2b94-117">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="f2b94-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f2b94-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f2b94-118">Requirements</span></span>



| <span data-ttu-id="f2b94-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f2b94-119">Requirement</span></span> | <span data-ttu-id="f2b94-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f2b94-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b94-121">Header</span><span class="sxs-lookup"><span data-stu-id="f2b94-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f2b94-122"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2b94-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2b94-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f2b94-123">Library</span></span><br/> | <dl> <span data-ttu-id="f2b94-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f2b94-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2b94-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f2b94-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b94-126">**Класс Кмедиапоситион**</span><span class="sxs-lookup"><span data-stu-id="f2b94-126">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




