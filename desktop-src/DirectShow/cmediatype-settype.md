---
description: Метод Сеттипе задает основной тип.
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: Кмедиатипе. Сеттипе, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfcf6ca634bce92701eb89f26dcfb6bdfb51f698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669191"
---
# <a name="cmediatypesettype-method"></a><span data-ttu-id="deee4-103">Кмедиатипе. Сеттипе, метод</span><span class="sxs-lookup"><span data-stu-id="deee4-103">CMediaType.SetType method</span></span>

<span data-ttu-id="deee4-104">`SetType`Метод задает основной тип.</span><span class="sxs-lookup"><span data-stu-id="deee4-104">The `SetType` method specifies the major type.</span></span>

## <a name="syntax"></a><span data-ttu-id="deee4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="deee4-105">Syntax</span></span>


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a><span data-ttu-id="deee4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="deee4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deee4-107">*птипе*</span><span class="sxs-lookup"><span data-stu-id="deee4-107">*ptype*</span></span> 
</dt> <dd>

<span data-ttu-id="deee4-108">Указатель на **идентификатор GUID** , указывающий основной тип.</span><span class="sxs-lookup"><span data-stu-id="deee4-108">Pointer to a **GUID** that specifies the major type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deee4-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="deee4-109">Return value</span></span>

<span data-ttu-id="deee4-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="deee4-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="deee4-111">Требования</span><span class="sxs-lookup"><span data-stu-id="deee4-111">Requirements</span></span>



| <span data-ttu-id="deee4-112">Требование</span><span class="sxs-lookup"><span data-stu-id="deee4-112">Requirement</span></span> | <span data-ttu-id="deee4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="deee4-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deee4-114">Header</span><span class="sxs-lookup"><span data-stu-id="deee4-114">Header</span></span><br/>  | <dl> <span data-ttu-id="deee4-115"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="deee4-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="deee4-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="deee4-116">Library</span></span><br/> | <dl> <span data-ttu-id="deee4-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="deee4-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deee4-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="deee4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deee4-119">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="deee4-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




