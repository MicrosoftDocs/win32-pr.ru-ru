---
description: Метод Аддбефореи вставляет элемент перед указанной позицией.
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: Кбаселист. Аддбефореи, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBeforeI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6996d2fd3ed0cad07a442530e3ae77470aaf6890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668615"
---
# <a name="cbaselistaddbeforei-method"></a><span data-ttu-id="c0e27-103">Кбаселист. Аддбефореи, метод</span><span class="sxs-lookup"><span data-stu-id="c0e27-103">CBaseList.AddBeforeI method</span></span>

<span data-ttu-id="c0e27-104">`AddBeforeI`Метод вставляет элемент перед указанной позицией.</span><span class="sxs-lookup"><span data-stu-id="c0e27-104">The `AddBeforeI` method inserts an item before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0e27-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0e27-105">Syntax</span></span>


```C++
POSITION AddBeforeI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="c0e27-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0e27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0e27-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="c0e27-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="c0e27-108">Позиция, до которой нужно добавить элемент.</span><span class="sxs-lookup"><span data-stu-id="c0e27-108">Position before which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="c0e27-109">*побж*</span><span class="sxs-lookup"><span data-stu-id="c0e27-109">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="c0e27-110">Указатель на элемент.</span><span class="sxs-lookup"><span data-stu-id="c0e27-110">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0e27-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0e27-111">Return value</span></span>

<span data-ttu-id="c0e27-112">Возвращает индикатор позиции для вставленного элемента.</span><span class="sxs-lookup"><span data-stu-id="c0e27-112">Returns the position indicator for the inserted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0e27-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0e27-113">Remarks</span></span>

<span data-ttu-id="c0e27-114">Если *POS* имеет **значение NULL**, этот метод добавляет элемент в конец списка (эквивалентно вызову метода [**кбаселист:: аддтаили**](cbaselist-addtaili.md) ).</span><span class="sxs-lookup"><span data-stu-id="c0e27-114">If *pos* is **NULL**, this method adds the item to the tail of the list (equivalent to calling the [**CBaseList::AddTailI**](cbaselist-addtaili.md) method).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0e27-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c0e27-115">Requirements</span></span>



| <span data-ttu-id="c0e27-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c0e27-116">Requirement</span></span> | <span data-ttu-id="c0e27-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c0e27-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0e27-118">Header</span><span class="sxs-lookup"><span data-stu-id="c0e27-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c0e27-119"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0e27-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c0e27-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c0e27-120">Library</span></span><br/> | <dl> <span data-ttu-id="c0e27-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c0e27-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0e27-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0e27-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0e27-123">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="c0e27-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




