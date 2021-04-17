---
description: Оператор = назначает новое время ссылки.
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: Крефтиме. operator =-метод (Рефтиме. h)
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
ms.openlocfilehash: 8d93a57211c3bc7d787e68f70f36be868ff64449
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679875"
---
# <a name="creftimeoperator-method-reftimeh"></a><span data-ttu-id="97c4b-103">Крефтиме. operator =-метод (Рефтиме. h)</span><span class="sxs-lookup"><span data-stu-id="97c4b-103">CRefTime.operator= method (Reftime.h)</span></span>

<span data-ttu-id="97c4b-104">Оператор = назначает новое время ссылки.</span><span class="sxs-lookup"><span data-stu-id="97c4b-104">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c4b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97c4b-105">Syntax</span></span>


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a><span data-ttu-id="97c4b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="97c4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c4b-107">*залив*</span><span class="sxs-lookup"><span data-stu-id="97c4b-107">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="97c4b-108">Новое время ссылки в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="97c4b-108">New reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c4b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97c4b-109">Return value</span></span>

<span data-ttu-id="97c4b-110">Возвращает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="97c4b-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c4b-111">Требования</span><span class="sxs-lookup"><span data-stu-id="97c4b-111">Requirements</span></span>



| <span data-ttu-id="97c4b-112">Требование</span><span class="sxs-lookup"><span data-stu-id="97c4b-112">Requirement</span></span> | <span data-ttu-id="97c4b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="97c4b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97c4b-114">Header</span><span class="sxs-lookup"><span data-stu-id="97c4b-114">Header</span></span><br/>  | <dl> <span data-ttu-id="97c4b-115"><dt>Рефтиме. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97c4b-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="97c4b-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="97c4b-116">Library</span></span><br/> | <dl> <span data-ttu-id="97c4b-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="97c4b-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




