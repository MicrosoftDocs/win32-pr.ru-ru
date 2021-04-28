---
description: Метод конструктора Кункновн. Кункновн.
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Конструктор Кункновн. Кункновн (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32859871f8ef69ce357fe204f0741356314fbb06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084612"
---
# <a name="cunknowncunknown-constructor"></a><span data-ttu-id="34eb5-103">Кункновн. Кункновн, конструктор</span><span class="sxs-lookup"><span data-stu-id="34eb5-103">CUnknown.CUnknown constructor</span></span>

<span data-ttu-id="34eb5-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="34eb5-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="34eb5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34eb5-105">Syntax</span></span>


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="34eb5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="34eb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34eb5-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="34eb5-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="34eb5-108">Строка, содержащая имя объекта; используется в конструкторе [**кбасеобжект**](cbaseobject.md) для отладки.</span><span class="sxs-lookup"><span data-stu-id="34eb5-108">String containing the name of the object; used in the [**CBaseObject**](cbaseobject.md) constructor for debugging.</span></span>

</dd> <dt>

<span data-ttu-id="34eb5-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="34eb5-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="34eb5-110">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="34eb5-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="34eb5-111">Если объект является агрегатным, передайте указатель на интерфейс IUnknown объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="34eb5-111">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="34eb5-112">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="34eb5-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34eb5-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="34eb5-113">Remarks</span></span>

<span data-ttu-id="34eb5-114">Объект инициализируется с нулевым значением счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="34eb5-114">The object is initialized with a reference count of zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="34eb5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="34eb5-115">Requirements</span></span>



| <span data-ttu-id="34eb5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="34eb5-116">Requirement</span></span> | <span data-ttu-id="34eb5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="34eb5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34eb5-118">Header</span><span class="sxs-lookup"><span data-stu-id="34eb5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="34eb5-119"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34eb5-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34eb5-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="34eb5-120">Library</span></span><br/> | <dl> <span data-ttu-id="34eb5-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="34eb5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




