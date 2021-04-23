---
description: Оператор = назначает новое время ссылки. Этот метод использует параметр *LL* .
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: Крефтиме. operator = метод (Рефтиме. h) — параметр LL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d09cb957e06d8b075cff3d831a7f68fbbdf662a8
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187841"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a><span data-ttu-id="fa4eb-104">Крефтиме. operator = метод (Рефтиме. h) — параметр LL</span><span class="sxs-lookup"><span data-stu-id="fa4eb-104">CRefTime.operator= method (Reftime.h) - ll parameter</span></span>

<span data-ttu-id="fa4eb-105">Оператор = назначает новое время ссылки.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-105">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa4eb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa4eb-106">Syntax</span></span>


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a><span data-ttu-id="fa4eb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa4eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa4eb-108">*залив*</span><span class="sxs-lookup"><span data-stu-id="fa4eb-108">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="fa4eb-109">Новое время ссылки в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-109">New reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa4eb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa4eb-110">Return value</span></span>

<span data-ttu-id="fa4eb-111">Возвращает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="fa4eb-111">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa4eb-112">Требования</span><span class="sxs-lookup"><span data-stu-id="fa4eb-112">Requirements</span></span>



| <span data-ttu-id="fa4eb-113">Требование</span><span class="sxs-lookup"><span data-stu-id="fa4eb-113">Requirement</span></span> | <span data-ttu-id="fa4eb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fa4eb-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa4eb-115">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fa4eb-115">Header</span></span>  | <span data-ttu-id="fa4eb-116">Рефтиме. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="fa4eb-116">Reftime.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="fa4eb-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fa4eb-117">Library</span></span> | <span data-ttu-id="fa4eb-118">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="fa4eb-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



 

 




