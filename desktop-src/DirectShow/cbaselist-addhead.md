---
description: Метод Аддхеад вставляет еще один список в начале этого списка.
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: Кбаселист. Аддхеад, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a262f2bcfb7c40671fd472ecd7d3f887b1db4224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668613"
---
# <a name="cbaselistaddhead-method"></a><span data-ttu-id="27a2d-103">Кбаселист. Аддхеад, метод</span><span class="sxs-lookup"><span data-stu-id="27a2d-103">CBaseList.AddHead method</span></span>

<span data-ttu-id="27a2d-104">`AddHead`Метод вставляет еще один список в начале этого списка.</span><span class="sxs-lookup"><span data-stu-id="27a2d-104">The `AddHead` method inserts another list at the front of this list.</span></span>

## <a name="syntax"></a><span data-ttu-id="27a2d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27a2d-105">Syntax</span></span>


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="27a2d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="27a2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27a2d-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="27a2d-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="27a2d-108">Указатель на список элементов для добавления.</span><span class="sxs-lookup"><span data-stu-id="27a2d-108">Pointer to the list of items to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27a2d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27a2d-109">Return value</span></span>

<span data-ttu-id="27a2d-110">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="27a2d-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="27a2d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27a2d-111">Remarks</span></span>

<span data-ttu-id="27a2d-112">В случае сбоя метода некоторые элементы могут быть добавлены в список.</span><span class="sxs-lookup"><span data-stu-id="27a2d-112">If the method fails, some items might have been added to the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="27a2d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="27a2d-113">Requirements</span></span>



| <span data-ttu-id="27a2d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="27a2d-114">Requirement</span></span> | <span data-ttu-id="27a2d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="27a2d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27a2d-116">Header</span><span class="sxs-lookup"><span data-stu-id="27a2d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="27a2d-117"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27a2d-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="27a2d-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="27a2d-118">Library</span></span><br/> | <dl> <span data-ttu-id="27a2d-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="27a2d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27a2d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27a2d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27a2d-121">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="27a2d-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




