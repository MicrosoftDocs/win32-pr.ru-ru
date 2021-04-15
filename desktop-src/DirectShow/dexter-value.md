---
description: Определяет свойство, которое должно быть задано для перехода или воздействия, а также количество различных значений, принимаемых свойством на протяжении перехода или воздействия.
ms.assetid: 3b1c35cf-f1f7-4f2c-8d94-1aaae4116833
title: Структура DEXTER_VALUE (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_VALUE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 930b828e1b715cfcb53275192ed76a7df7d116ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675733"
---
# <a name="dexter_value-structure"></a><span data-ttu-id="1109f-103">\_Структура значения Декстер</span><span class="sxs-lookup"><span data-stu-id="1109f-103">DEXTER\_VALUE structure</span></span>

> [!Note]  
> <span data-ttu-id="1109f-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1109f-104">\[Deprecated.</span></span> <span data-ttu-id="1109f-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1109f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1109f-106">Определяет свойство, которое должно быть задано для перехода или воздействия, а также количество различных значений, принимаемых свойством на протяжении перехода или воздействия.</span><span class="sxs-lookup"><span data-stu-id="1109f-106">Identifies a property that is to be set on a transition or effect, along with the number of distinct values that the property assumes over the duration of the transition or effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="1109f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1109f-107">Syntax</span></span>


```C++
typedef struct {
  VARIANT        v;
  REFERENCE_TIME rt;
  DWORD          dwInterp;
} DEXTER_VALUE;
```



## <a name="members"></a><span data-ttu-id="1109f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="1109f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1109f-109">**3,3**</span><span class="sxs-lookup"><span data-stu-id="1109f-109">**v**</span></span>
</dt> <dd>

<span data-ttu-id="1109f-110">Значение свойства.</span><span class="sxs-lookup"><span data-stu-id="1109f-110">Value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="1109f-111">**прямоуголь**</span><span class="sxs-lookup"><span data-stu-id="1109f-111">**rt**</span></span>
</dt> <dd>

<span data-ttu-id="1109f-112">Время, когда свойство принимает значение относительно начала перехода или воздействия.</span><span class="sxs-lookup"><span data-stu-id="1109f-112">Time at which the property assumes the value, relative to the start of the transition or effect.</span></span>

</dd> <dt>

<span data-ttu-id="1109f-113">**двинтерп**</span><span class="sxs-lookup"><span data-stu-id="1109f-113">**dwInterp**</span></span>
</dt> <dd>

<span data-ttu-id="1109f-114">Флаг, указывающий, как выполняется свойство из предыдущего значения в это значение.</span><span class="sxs-lookup"><span data-stu-id="1109f-114">Flag indicating how the property progresses from the previous value to this value.</span></span> <span data-ttu-id="1109f-115">Должна быть одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="1109f-115">Must be one of the following:</span></span>



| <span data-ttu-id="1109f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1109f-116">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="1109f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1109f-117">Meaning</span></span>                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <span data-ttu-id="1109f-118"><dt>**ДЕКСТЕРФ \_ Переход**</dt></span><span class="sxs-lookup"><span data-stu-id="1109f-118"><dt>**DEXTERF\_JUMP**</dt></span></span> </dl>                      | <span data-ttu-id="1109f-119">Свойство немедленно переходит к новому значению в указанное время.</span><span class="sxs-lookup"><span data-stu-id="1109f-119">The property jumps instantly to the new value at the specified time.</span></span><br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <span data-ttu-id="1109f-120"><dt>**ДЕКСТЕРФ \_ интерполяция**</dt></span><span class="sxs-lookup"><span data-stu-id="1109f-120"><dt>**DEXTERF\_INTERPOLATE**</dt></span></span> </dl> | <span data-ttu-id="1109f-121">Свойство интерполируются линейно по времени от предыдущего значения.</span><span class="sxs-lookup"><span data-stu-id="1109f-121">The property is interpolated linearly over time from the previous value.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1109f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1109f-122">Requirements</span></span>



| <span data-ttu-id="1109f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1109f-123">Requirement</span></span> | <span data-ttu-id="1109f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1109f-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1109f-125">Header</span><span class="sxs-lookup"><span data-stu-id="1109f-125">Header</span></span><br/> | <dl> <span data-ttu-id="1109f-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="1109f-126"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1109f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1109f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1109f-128">**ипропертисеттер**</span><span class="sxs-lookup"><span data-stu-id="1109f-128">**IPropertySetter**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="1109f-129">**Декстер, \_ параметр**</span><span class="sxs-lookup"><span data-stu-id="1109f-129">**DEXTER\_PARAM**</span></span>](dexter-param.md)
</dt> </dl>

 

 




