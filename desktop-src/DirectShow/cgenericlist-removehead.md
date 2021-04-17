---
description: Метод Ремовехеад удаляет первый элемент из списка.
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: Кженериклист. Ремовехеад, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da9267d6b3e0c3196b3a9d1e873f222649b66684
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657557"
---
# <a name="cgenericlistremovehead-method"></a><span data-ttu-id="fa4fa-103">Кженериклист. Ремовехеад, метод</span><span class="sxs-lookup"><span data-stu-id="fa4fa-103">CGenericList.RemoveHead method</span></span>

<span data-ttu-id="fa4fa-104">`RemoveHead`Метод удаляет первый элемент из списка.</span><span class="sxs-lookup"><span data-stu-id="fa4fa-104">The `RemoveHead` method removes the first item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa4fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa4fa-105">Syntax</span></span>


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a><span data-ttu-id="fa4fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa4fa-106">Parameters</span></span>

<span data-ttu-id="fa4fa-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fa4fa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa4fa-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa4fa-108">Return value</span></span>

<span data-ttu-id="fa4fa-109">Возвращает указатель на объект типа **Object** (тип шаблона) или **значение NULL** , если список пуст.</span><span class="sxs-lookup"><span data-stu-id="fa4fa-109">Returns a pointer to an object of type **OBJECT** (the template type), or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa4fa-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa4fa-110">Remarks</span></span>

<span data-ttu-id="fa4fa-111">Этот метод удаляет узел списка, но не элемент, содержащийся в узле.</span><span class="sxs-lookup"><span data-stu-id="fa4fa-111">This method deletes the list node, but not the item that the node contains.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa4fa-112">Требования</span><span class="sxs-lookup"><span data-stu-id="fa4fa-112">Requirements</span></span>



| <span data-ttu-id="fa4fa-113">Требование</span><span class="sxs-lookup"><span data-stu-id="fa4fa-113">Requirement</span></span> | <span data-ttu-id="fa4fa-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fa4fa-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa4fa-115">Header</span><span class="sxs-lookup"><span data-stu-id="fa4fa-115">Header</span></span><br/>  | <dl> <span data-ttu-id="fa4fa-116"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa4fa-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="fa4fa-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fa4fa-117">Library</span></span><br/> | <dl> <span data-ttu-id="fa4fa-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fa4fa-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa4fa-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa4fa-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa4fa-120">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="fa4fa-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




