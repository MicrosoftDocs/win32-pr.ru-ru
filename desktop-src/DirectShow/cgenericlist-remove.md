---
description: Метод Remove удаляет элемент в указанной позиции.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: Метод Кженериклист. Remove (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5fc3d0cd76cd78c83fa210d8b91ba97b93b92f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657558"
---
# <a name="cgenericlistremove-method"></a><span data-ttu-id="1f9f5-103">Кженериклист. Remove, метод</span><span class="sxs-lookup"><span data-stu-id="1f9f5-103">CGenericList.Remove method</span></span>

<span data-ttu-id="1f9f5-104">`Remove`Метод удаляет элемент в указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="1f9f5-104">The `Remove` method removes the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f9f5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f9f5-105">Syntax</span></span>


```C++
OBJECT* Remove(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="1f9f5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f9f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f9f5-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="1f9f5-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="1f9f5-108">Значение позиции, указывающее удаляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="1f9f5-108">POSITION value indicating the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f9f5-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f9f5-109">Return value</span></span>

<span data-ttu-id="1f9f5-110">Возвращает указатель на объект типа **Object** (тип шаблона).</span><span class="sxs-lookup"><span data-stu-id="1f9f5-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="1f9f5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f9f5-111">Remarks</span></span>

<span data-ttu-id="1f9f5-112">Этот метод удаляет узел из списка, но не удаляет элемент, содержащийся в этом узле.</span><span class="sxs-lookup"><span data-stu-id="1f9f5-112">This method deletes the node from the list, but does not delete the item contained in that node.</span></span>

<span data-ttu-id="1f9f5-113">Если *POS* имеет **значение NULL**, метод возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1f9f5-113">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f9f5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1f9f5-114">Requirements</span></span>



| <span data-ttu-id="1f9f5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1f9f5-115">Requirement</span></span> | <span data-ttu-id="1f9f5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1f9f5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f9f5-117">Header</span><span class="sxs-lookup"><span data-stu-id="1f9f5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1f9f5-118"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f9f5-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1f9f5-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1f9f5-119">Library</span></span><br/> | <dl> <span data-ttu-id="1f9f5-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1f9f5-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f9f5-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f9f5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f9f5-122">**Класс Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="1f9f5-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




