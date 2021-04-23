---
description: Метод Ремовеи удаляет элемент в указанной позиции.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: Кбаселист. Ремовеи, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4511a9867f61596572c959a3d763eb56d862311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668997"
---
# <a name="cbaselistremovei-method"></a><span data-ttu-id="ea160-103">Кбаселист. Ремовеи, метод</span><span class="sxs-lookup"><span data-stu-id="ea160-103">CBaseList.RemoveI method</span></span>

<span data-ttu-id="ea160-104">`RemoveI`Метод удаляет элемент в указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="ea160-104">The `RemoveI` method removes the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea160-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea160-105">Syntax</span></span>


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="ea160-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea160-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea160-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="ea160-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="ea160-108">Значение позиции, указывающее удаляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="ea160-108">POSITION value indicating the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea160-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea160-109">Return value</span></span>

<span data-ttu-id="ea160-110">Возвращает указатель на элемент.</span><span class="sxs-lookup"><span data-stu-id="ea160-110">Returns a pointer to the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea160-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea160-111">Remarks</span></span>

<span data-ttu-id="ea160-112">Этот метод удаляет узел из списка, но не удаляет элемент, содержащийся в этом узле.</span><span class="sxs-lookup"><span data-stu-id="ea160-112">This method deletes the node from the list, but does not delete the item contained in that node.</span></span>

<span data-ttu-id="ea160-113">Если *POS* имеет **значение NULL**, метод возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ea160-113">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea160-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ea160-114">Requirements</span></span>



| <span data-ttu-id="ea160-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ea160-115">Requirement</span></span> | <span data-ttu-id="ea160-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ea160-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea160-117">Header</span><span class="sxs-lookup"><span data-stu-id="ea160-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ea160-118"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea160-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ea160-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ea160-119">Library</span></span><br/> | <dl> <span data-ttu-id="ea160-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ea160-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea160-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea160-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea160-122">**Класс Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="ea160-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




