---
description: Определяет расположение, в котором необходимо получить доступ к компоненту цвета или цвета для вычислений освещения.
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: Перечисление D3DMATERIALCOLORSOURCE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIALCOLORSOURCE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8877eece8e33c6508768b22c989e992cf8178823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703841"
---
# <a name="d3dmaterialcolorsource-enumeration"></a><span data-ttu-id="99dd0-103">Перечисление D3DMATERIALCOLORSOURCE</span><span class="sxs-lookup"><span data-stu-id="99dd0-103">D3DMATERIALCOLORSOURCE enumeration</span></span>

<span data-ttu-id="99dd0-104">Определяет расположение, в котором необходимо получить доступ к компоненту цвета или цвета для вычислений освещения.</span><span class="sxs-lookup"><span data-stu-id="99dd0-104">Defines the location at which a color or color component must be accessed for lighting calculations.</span></span>

## <a name="syntax"></a><span data-ttu-id="99dd0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99dd0-105">Syntax</span></span>


```C++
typedef enum D3DMATERIALCOLORSOURCE { 
  D3DMCS_MATERIAL     = 0,
  D3DMCS_COLOR1       = 1,
  D3DMCS_COLOR2       = 2,
  D3DMCS_FORCE_DWORD  = 0x7fffffff
} D3DMATERIALCOLORSOURCE, *LPD3DMATERIALCOLORSOURCE;
```



## <a name="constants"></a><span data-ttu-id="99dd0-106">Константы</span><span class="sxs-lookup"><span data-stu-id="99dd0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="99dd0-107"><span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**\_Материал D3DMCS**</span><span class="sxs-lookup"><span data-stu-id="99dd0-107"><span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**D3DMCS\_MATERIAL**</span></span>
</dt> <dd>

<span data-ttu-id="99dd0-108">Использовать цвет из текущего материала.</span><span class="sxs-lookup"><span data-stu-id="99dd0-108">Use the color from the current material.</span></span>

</dd> <dt>

<span data-ttu-id="99dd0-109"><span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS \_ COLOR1**</span><span class="sxs-lookup"><span data-stu-id="99dd0-109"><span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS\_COLOR1**</span></span>
</dt> <dd>

<span data-ttu-id="99dd0-110">Используйте рассеянный цвет вершины.</span><span class="sxs-lookup"><span data-stu-id="99dd0-110">Use the diffuse vertex color.</span></span>

</dd> <dt>

<span data-ttu-id="99dd0-111"><span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS \_ COLOR2**</span><span class="sxs-lookup"><span data-stu-id="99dd0-111"><span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS\_COLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="99dd0-112">Используйте цвет отраженной вершины.</span><span class="sxs-lookup"><span data-stu-id="99dd0-112">Use the specular vertex color.</span></span>

</dd> <dt>

<span data-ttu-id="99dd0-113"><span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="99dd0-113"><span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="99dd0-114">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="99dd0-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="99dd0-115">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="99dd0-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="99dd0-116">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="99dd0-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99dd0-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99dd0-117">Remarks</span></span>

<span data-ttu-id="99dd0-118">Эти флаги используются для установки значений следующих состояний отрисовки в перечислимом типе [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="99dd0-118">These flags are used to set the value of the following render states in the [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type.</span></span>

-   <span data-ttu-id="99dd0-119">D3DRS \_ амбиентматериалсаурце</span><span class="sxs-lookup"><span data-stu-id="99dd0-119">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="99dd0-120">D3DRS \_ диффусематериалсаурце</span><span class="sxs-lookup"><span data-stu-id="99dd0-120">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="99dd0-121">D3DRS \_ емиссивематериалсаурце</span><span class="sxs-lookup"><span data-stu-id="99dd0-121">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>
-   <span data-ttu-id="99dd0-122">D3DRS \_ спекуларматериалсаурце</span><span class="sxs-lookup"><span data-stu-id="99dd0-122">D3DRS\_SPECULARMATERIALSOURCE</span></span>

## <a name="requirements"></a><span data-ttu-id="99dd0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="99dd0-123">Requirements</span></span>



| <span data-ttu-id="99dd0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="99dd0-124">Requirement</span></span> | <span data-ttu-id="99dd0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="99dd0-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99dd0-126">Header</span><span class="sxs-lookup"><span data-stu-id="99dd0-126">Header</span></span><br/> | <dl> <span data-ttu-id="99dd0-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="99dd0-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99dd0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99dd0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99dd0-129">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="99dd0-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="99dd0-130">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="99dd0-130">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
