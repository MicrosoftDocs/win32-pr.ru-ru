---
description: Метод Сетсубтипе задает подтип.
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: Кмедиатипе. Сетсубтипе, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6474777b1b2e91ce0b676fdc7dbd572d7c622f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665472"
---
# <a name="cmediatypesetsubtype-method"></a><span data-ttu-id="7f13a-103">Кмедиатипе. Сетсубтипе, метод</span><span class="sxs-lookup"><span data-stu-id="7f13a-103">CMediaType.SetSubtype method</span></span>

<span data-ttu-id="7f13a-104">`SetSubtype`Метод задает подтип.</span><span class="sxs-lookup"><span data-stu-id="7f13a-104">The `SetSubtype` method specifies the subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f13a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f13a-105">Syntax</span></span>


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a><span data-ttu-id="7f13a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f13a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f13a-107">*псубтипе*</span><span class="sxs-lookup"><span data-stu-id="7f13a-107">*psubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="7f13a-108">Указатель на **идентификатор GUID** , указывающий подтип.</span><span class="sxs-lookup"><span data-stu-id="7f13a-108">Pointer to a **GUID** that specifies the subtype.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f13a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f13a-109">Return value</span></span>

<span data-ttu-id="7f13a-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7f13a-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f13a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="7f13a-111">Requirements</span></span>



| <span data-ttu-id="7f13a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="7f13a-112">Requirement</span></span> | <span data-ttu-id="7f13a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7f13a-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f13a-114">Header</span><span class="sxs-lookup"><span data-stu-id="7f13a-114">Header</span></span><br/>  | <dl> <span data-ttu-id="7f13a-115"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f13a-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="7f13a-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7f13a-116">Library</span></span><br/> | <dl> <span data-ttu-id="7f13a-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7f13a-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f13a-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f13a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f13a-119">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="7f13a-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




