---
description: Определяет поддерживаемые операции смешения. Определения терминов см. в разделе Примечания.
ms.assetid: ae750d84-ed7d-4a76-bf64-eae8828c66c7
title: Перечисление D3DBLENDOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLENDOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3ad23d3fb2a93734047f55a46c14335069c95ea9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713576"
---
# <a name="d3dblendop-enumeration"></a><span data-ttu-id="2f589-104">Перечисление D3DBLENDOP</span><span class="sxs-lookup"><span data-stu-id="2f589-104">D3DBLENDOP enumeration</span></span>

<span data-ttu-id="2f589-105">Определяет поддерживаемые операции смешения.</span><span class="sxs-lookup"><span data-stu-id="2f589-105">Defines the supported blend operations.</span></span> <span data-ttu-id="2f589-106">Определения терминов см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="2f589-106">See Remarks for definitions of terms.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f589-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f589-107">Syntax</span></span>


```C++
typedef enum D3DBLENDOP { 
  D3DBLENDOP_ADD          = 1,
  D3DBLENDOP_SUBTRACT     = 2,
  D3DBLENDOP_REVSUBTRACT  = 3,
  D3DBLENDOP_MIN          = 4,
  D3DBLENDOP_MAX          = 5,
  D3DBLENDOP_FORCE_DWORD  = 0x7fffffff
} D3DBLENDOP, *LPD3DBLENDOP;
```



## <a name="constants"></a><span data-ttu-id="2f589-108">Константы</span><span class="sxs-lookup"><span data-stu-id="2f589-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2f589-109"><span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP \_ Добавить**</span><span class="sxs-lookup"><span data-stu-id="2f589-109"><span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP\_ADD**</span></span>
</dt> <dd>

<span data-ttu-id="2f589-110">Результатом является назначение, добавленное в источник.</span><span class="sxs-lookup"><span data-stu-id="2f589-110">The result is the destination added to the source.</span></span> <span data-ttu-id="2f589-111">Result = источник + назначение</span><span class="sxs-lookup"><span data-stu-id="2f589-111">Result = Source + Destination</span></span>

</dd> <dt>

<span data-ttu-id="2f589-112"><span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**\_Вычитание D3DBLENDOP**</span><span class="sxs-lookup"><span data-stu-id="2f589-112"><span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**D3DBLENDOP\_SUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="2f589-113">Результат — это назначение, вычитаемое из в источник.</span><span class="sxs-lookup"><span data-stu-id="2f589-113">The result is the destination subtracted from to the source.</span></span> <span data-ttu-id="2f589-114">Result = источник-назначение</span><span class="sxs-lookup"><span data-stu-id="2f589-114">Result = Source - Destination</span></span>

</dd> <dt>

<span data-ttu-id="2f589-115"><span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP \_ ревсубтракт**</span><span class="sxs-lookup"><span data-stu-id="2f589-115"><span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP\_REVSUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="2f589-116">Результат — источник, вычитаемый из назначения.</span><span class="sxs-lookup"><span data-stu-id="2f589-116">The result is the source subtracted from the destination.</span></span> <span data-ttu-id="2f589-117">Result = целевой источник</span><span class="sxs-lookup"><span data-stu-id="2f589-117">Result = Destination - Source</span></span>

</dd> <dt>

<span data-ttu-id="2f589-118"><span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP \_ мин**</span><span class="sxs-lookup"><span data-stu-id="2f589-118"><span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="2f589-119">Результат — минимум источника и назначения.</span><span class="sxs-lookup"><span data-stu-id="2f589-119">The result is the minimum of the source and destination.</span></span> <span data-ttu-id="2f589-120">Результат = MIN (источник, назначение)</span><span class="sxs-lookup"><span data-stu-id="2f589-120">Result = MIN(Source, Destination)</span></span>

</dd> <dt>

<span data-ttu-id="2f589-121"><span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP \_ Max**</span><span class="sxs-lookup"><span data-stu-id="2f589-121"><span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="2f589-122">Результат — максимум источника и назначения.</span><span class="sxs-lookup"><span data-stu-id="2f589-122">The result is the maximum of the source and destination.</span></span> <span data-ttu-id="2f589-123">Result = MAX (источник, назначение)</span><span class="sxs-lookup"><span data-stu-id="2f589-123">Result = MAX(Source, Destination)</span></span>

</dd> <dt>

<span data-ttu-id="2f589-124"><span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2f589-124"><span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="2f589-125">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="2f589-125">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="2f589-126">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="2f589-126">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="2f589-127">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="2f589-127">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f589-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f589-128">Remarks</span></span>

<span data-ttu-id="2f589-129">Источник, назначение и результат определяются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2f589-129">Source, Destination, and Result are defined as:</span></span>



| <span data-ttu-id="2f589-130">Термин</span><span class="sxs-lookup"><span data-stu-id="2f589-130">Term</span></span>        | <span data-ttu-id="2f589-131">Тип</span><span class="sxs-lookup"><span data-stu-id="2f589-131">Type</span></span>   | <span data-ttu-id="2f589-132">Описание</span><span class="sxs-lookup"><span data-stu-id="2f589-132">Description</span></span>                                                            |
|-------------|--------|------------------------------------------------------------------------|
| <span data-ttu-id="2f589-133">Источник</span><span class="sxs-lookup"><span data-stu-id="2f589-133">Source</span></span>      | <span data-ttu-id="2f589-134">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2f589-134">Input</span></span>  | <span data-ttu-id="2f589-135">Цвет исходного пикселя перед операцией.</span><span class="sxs-lookup"><span data-stu-id="2f589-135">Color of the source pixel before the operation.</span></span>                        |
| <span data-ttu-id="2f589-136">Назначение</span><span class="sxs-lookup"><span data-stu-id="2f589-136">Destination</span></span> | <span data-ttu-id="2f589-137">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2f589-137">Input</span></span>  | <span data-ttu-id="2f589-138">Цвет пикселя в целевом буфере перед операцией.</span><span class="sxs-lookup"><span data-stu-id="2f589-138">Color of the pixel in the destination buffer before the operation.</span></span>     |
| <span data-ttu-id="2f589-139">Результат</span><span class="sxs-lookup"><span data-stu-id="2f589-139">Result</span></span>      | <span data-ttu-id="2f589-140">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="2f589-140">Output</span></span> | <span data-ttu-id="2f589-141">Возвращаемое значение, которое является смешением цвета, полученным в результате операции.</span><span class="sxs-lookup"><span data-stu-id="2f589-141">Returned value that is the blended color resulting from the operation.</span></span> |



 

<span data-ttu-id="2f589-142">Этот перечислимый тип определяет значения, используемые следующими состояниями визуализации:</span><span class="sxs-lookup"><span data-stu-id="2f589-142">This enumerated type defines values used by the following render states:</span></span>

-   <span data-ttu-id="2f589-143">D3DRS \_ блендоп</span><span class="sxs-lookup"><span data-stu-id="2f589-143">D3DRS\_BLENDOP</span></span>
-   <span data-ttu-id="2f589-144">D3DRS \_ блендопалфа</span><span class="sxs-lookup"><span data-stu-id="2f589-144">D3DRS\_BLENDOPALPHA</span></span>

## <a name="requirements"></a><span data-ttu-id="2f589-145">Требования</span><span class="sxs-lookup"><span data-stu-id="2f589-145">Requirements</span></span>



| <span data-ttu-id="2f589-146">Требование</span><span class="sxs-lookup"><span data-stu-id="2f589-146">Requirement</span></span> | <span data-ttu-id="2f589-147">Значение</span><span class="sxs-lookup"><span data-stu-id="2f589-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f589-148">Header</span><span class="sxs-lookup"><span data-stu-id="2f589-148">Header</span></span><br/> | <dl> <span data-ttu-id="2f589-149"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f589-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f589-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f589-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f589-151">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="2f589-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="2f589-152">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="2f589-152">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="2f589-153">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="2f589-153">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
