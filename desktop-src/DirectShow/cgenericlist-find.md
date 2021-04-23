---
description: Метод Find извлекает первую позицию, содержащую указанный элемент.
ms.assetid: 8e2a3e5d-96e6-4f40-8e2a-4dc8c21088cd
title: Метод Кженериклист. Find (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Find
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a21f16e25d8a2ebba4494a850bc456a7b579f2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657566"
---
# <a name="cgenericlistfind-method"></a><span data-ttu-id="ca193-103">Кженериклист. Find, метод</span><span class="sxs-lookup"><span data-stu-id="ca193-103">CGenericList.Find method</span></span>

<span data-ttu-id="ca193-104">`Find`Метод извлекает первую позицию, содержащую указанный элемент.</span><span class="sxs-lookup"><span data-stu-id="ca193-104">The `Find` method retrieves the first position that holds the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca193-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca193-105">Syntax</span></span>


```C++
POSITION Find(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="ca193-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca193-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca193-107">*побж*</span><span class="sxs-lookup"><span data-stu-id="ca193-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="ca193-108">Указатель на объект типа **Object** (тип шаблона).</span><span class="sxs-lookup"><span data-stu-id="ca193-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca193-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca193-109">Return value</span></span>

<span data-ttu-id="ca193-110">Возвращает значение позиции или **значение NULL** , если элемент отсутствует в списке.</span><span class="sxs-lookup"><span data-stu-id="ca193-110">Returns a POSITION value, or **NULL** if the item is not in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca193-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ca193-111">Requirements</span></span>



| <span data-ttu-id="ca193-112">Требование</span><span class="sxs-lookup"><span data-stu-id="ca193-112">Requirement</span></span> | <span data-ttu-id="ca193-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ca193-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca193-114">Header</span><span class="sxs-lookup"><span data-stu-id="ca193-114">Header</span></span><br/>  | <dl> <span data-ttu-id="ca193-115"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca193-115"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ca193-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ca193-116">Library</span></span><br/> | <dl> <span data-ttu-id="ca193-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ca193-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca193-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca193-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca193-119">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="ca193-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




