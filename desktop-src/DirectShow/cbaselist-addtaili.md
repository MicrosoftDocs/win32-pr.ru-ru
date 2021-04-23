---
description: Метод Аддтаили добавляет элемент в конец списка.
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: Кбаселист. Аддтаили, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c702256d75a2de6f914838f5c3412a4308a7241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657718"
---
# <a name="cbaselistaddtaili-method"></a><span data-ttu-id="cd98b-103">Кбаселист. Аддтаили, метод</span><span class="sxs-lookup"><span data-stu-id="cd98b-103">CBaseList.AddTailI method</span></span>

<span data-ttu-id="cd98b-104">`AddTailI`Метод добавляет элемент в конец списка.</span><span class="sxs-lookup"><span data-stu-id="cd98b-104">The `AddTailI` method adds an item to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd98b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd98b-105">Syntax</span></span>


```C++
POSITION AddTailI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="cd98b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd98b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd98b-107">*побж*</span><span class="sxs-lookup"><span data-stu-id="cd98b-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="cd98b-108">Указатель на элемент.</span><span class="sxs-lookup"><span data-stu-id="cd98b-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd98b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd98b-109">Return value</span></span>

<span data-ttu-id="cd98b-110">Возвращает значение позиции для новой позиции хвоста.</span><span class="sxs-lookup"><span data-stu-id="cd98b-110">Returns a POSITION value for the new tail position.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd98b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd98b-111">Remarks</span></span>

<span data-ttu-id="cd98b-112">Если метод завершается с ошибкой, возвращается **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="cd98b-112">If the method fails, it returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd98b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="cd98b-113">Requirements</span></span>



| <span data-ttu-id="cd98b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="cd98b-114">Requirement</span></span> | <span data-ttu-id="cd98b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="cd98b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd98b-116">Header</span><span class="sxs-lookup"><span data-stu-id="cd98b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cd98b-117"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd98b-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cd98b-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cd98b-118">Library</span></span><br/> | <dl> <span data-ttu-id="cd98b-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cd98b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd98b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd98b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd98b-121">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="cd98b-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




