---
description: Метод конструктора.
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
ms.openlocfilehash: b500e7f12a2242b6c05367bc061f50680d2d608b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657077"
---
# <a name="cunknowncunknown-constructor"></a><span data-ttu-id="867d9-103">Кункновн. Кункновн, конструктор</span><span class="sxs-lookup"><span data-stu-id="867d9-103">CUnknown.CUnknown constructor</span></span>

<span data-ttu-id="867d9-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="867d9-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="867d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="867d9-105">Syntax</span></span>


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="867d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="867d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="867d9-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="867d9-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="867d9-108">Строка, содержащая имя объекта; используется в конструкторе [**кбасеобжект**](cbaseobject.md) для отладки.</span><span class="sxs-lookup"><span data-stu-id="867d9-108">String containing the name of the object; used in the [**CBaseObject**](cbaseobject.md) constructor for debugging.</span></span>

</dd> <dt>

<span data-ttu-id="867d9-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="867d9-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="867d9-110">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="867d9-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="867d9-111">Если объект является агрегатным, передайте указатель на интерфейс IUnknown объекта агрегирования.</span><span class="sxs-lookup"><span data-stu-id="867d9-111">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="867d9-112">В противном случае присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="867d9-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="867d9-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="867d9-113">Remarks</span></span>

<span data-ttu-id="867d9-114">Объект инициализируется с нулевым значением счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="867d9-114">The object is initialized with a reference count of zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="867d9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="867d9-115">Requirements</span></span>



| <span data-ttu-id="867d9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="867d9-116">Requirement</span></span> | <span data-ttu-id="867d9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="867d9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="867d9-118">Header</span><span class="sxs-lookup"><span data-stu-id="867d9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="867d9-119"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="867d9-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="867d9-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="867d9-120">Library</span></span><br/> | <dl> <span data-ttu-id="867d9-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="867d9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




