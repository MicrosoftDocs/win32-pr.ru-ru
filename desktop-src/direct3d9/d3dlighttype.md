---
description: Определяет тип освещения.
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: Перечисление D3DLIGHTTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHTTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 83c94db3126443f757f01a69d7d773417f70683a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703842"
---
# <a name="d3dlighttype-enumeration"></a><span data-ttu-id="cd96e-103">Перечисление D3DLIGHTTYPE</span><span class="sxs-lookup"><span data-stu-id="cd96e-103">D3DLIGHTTYPE enumeration</span></span>

<span data-ttu-id="cd96e-104">Определяет тип освещения.</span><span class="sxs-lookup"><span data-stu-id="cd96e-104">Defines the light type.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd96e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd96e-105">Syntax</span></span>


```C++
typedef enum D3DLIGHTTYPE { 
  D3DLIGHT_POINT        = 1,
  D3DLIGHT_SPOT         = 2,
  D3DLIGHT_DIRECTIONAL  = 3,
  D3DLIGHT_FORCE_DWORD  = 0x7fffffff
} D3DLIGHTTYPE, *LPD3DLIGHTTYPE;
```



## <a name="constants"></a><span data-ttu-id="cd96e-106">Константы</span><span class="sxs-lookup"><span data-stu-id="cd96e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cd96e-107"><span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**\_Точка D3DLIGHT**</span><span class="sxs-lookup"><span data-stu-id="cd96e-107"><span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**D3DLIGHT\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="cd96e-108">Light — это источник точки.</span><span class="sxs-lookup"><span data-stu-id="cd96e-108">Light is a point source.</span></span> <span data-ttu-id="cd96e-109">Источник содержит место в пространстве и испускаемое освещение во всех направлениях.</span><span class="sxs-lookup"><span data-stu-id="cd96e-109">The light has a position in space and radiates light in all directions.</span></span>

</dd> <dt>

<span data-ttu-id="cd96e-110"><span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT \_**</span><span class="sxs-lookup"><span data-stu-id="cd96e-110"><span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="cd96e-111">Light — это источник Spotlight.</span><span class="sxs-lookup"><span data-stu-id="cd96e-111">Light is a spotlight source.</span></span> <span data-ttu-id="cd96e-112">Этот источник подобен точечному излучению, за исключением того, что освещения ограничен конусом.</span><span class="sxs-lookup"><span data-stu-id="cd96e-112">This light is like a point light, except that the illumination is limited to a cone.</span></span> <span data-ttu-id="cd96e-113">Этот тип освещения имеет направление и несколько других параметров, определяющих форму конуса, который он создает.</span><span class="sxs-lookup"><span data-stu-id="cd96e-113">This light type has a direction and several other parameters that determine the shape of the cone it produces.</span></span> <span data-ttu-id="cd96e-114">Дополнительные сведения об этих параметрах см. в разделе Структура [**D3DLIGHT9**](d3dlight9.md) .</span><span class="sxs-lookup"><span data-stu-id="cd96e-114">For information about these parameters, see the [**D3DLIGHT9**](d3dlight9.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cd96e-115"><span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT \_ направление**</span><span class="sxs-lookup"><span data-stu-id="cd96e-115"><span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT\_DIRECTIONAL**</span></span>
</dt> <dd>

<span data-ttu-id="cd96e-116">Light — это направленный источник освещения.</span><span class="sxs-lookup"><span data-stu-id="cd96e-116">Light is a directional light source.</span></span> <span data-ttu-id="cd96e-117">Это эквивалентно использованию источника «точка-источник» с бесконечным расстоянием.</span><span class="sxs-lookup"><span data-stu-id="cd96e-117">This is equivalent to using a point light source at an infinite distance.</span></span>

</dd> <dt>

<span data-ttu-id="cd96e-118"><span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd96e-118"><span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="cd96e-119">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="cd96e-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="cd96e-120">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="cd96e-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="cd96e-121">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="cd96e-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd96e-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd96e-122">Remarks</span></span>

<span data-ttu-id="cd96e-123">Направленные источники света немного быстрее, чем источники света, но световые индикаторы выглядят немного лучше.</span><span class="sxs-lookup"><span data-stu-id="cd96e-123">Directional lights are slightly faster than point light sources, but point lights look a little better.</span></span> <span data-ttu-id="cd96e-124">Прожекторы предлагают интересные визуальные эффекты, но они потребляют много времени.</span><span class="sxs-lookup"><span data-stu-id="cd96e-124">Spotlights offer interesting visual effects but are computationally time-consuming.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd96e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="cd96e-125">Requirements</span></span>



| <span data-ttu-id="cd96e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="cd96e-126">Requirement</span></span> | <span data-ttu-id="cd96e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="cd96e-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd96e-128">Header</span><span class="sxs-lookup"><span data-stu-id="cd96e-128">Header</span></span><br/> | <dl> <span data-ttu-id="cd96e-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd96e-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd96e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd96e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd96e-131">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="cd96e-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="cd96e-132">**D3DLIGHT9**</span><span class="sxs-lookup"><span data-stu-id="cd96e-132">**D3DLIGHT9**</span></span>](d3dlight9.md)
</dt> </dl>

 

 




