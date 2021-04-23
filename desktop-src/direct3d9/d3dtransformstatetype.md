---
description: Определяет константы, описывающие значения состояния преобразования.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Перечисление D3DTRANSFORMSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRANSFORMSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c618e0e19bf7dd01dec73d35436f23189f9e78a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713599"
---
# <a name="d3dtransformstatetype-enumeration"></a><span data-ttu-id="ec7a5-103">Перечисление D3DTRANSFORMSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="ec7a5-103">D3DTRANSFORMSTATETYPE enumeration</span></span>

<span data-ttu-id="ec7a5-104">Определяет константы, описывающие значения состояния преобразования.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-104">Defines constants that describe transformation state values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec7a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec7a5-105">Syntax</span></span>


```C++
typedef enum D3DTRANSFORMSTATETYPE { 
  D3DTS_VIEW         = 2,
  D3DTS_PROJECTION   = 3,
  D3DTS_TEXTURE0     = 16,
  D3DTS_TEXTURE1     = 17,
  D3DTS_TEXTURE2     = 18,
  D3DTS_TEXTURE3     = 19,
  D3DTS_TEXTURE4     = 20,
  D3DTS_TEXTURE5     = 21,
  D3DTS_TEXTURE6     = 22,
  D3DTS_TEXTURE7     = 23,
  D3DTS_FORCE_DWORD  = 0x7fffffff
} D3DTRANSFORMSTATETYPE, *LPD3DTRANSFORMSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="ec7a5-106">Константы</span><span class="sxs-lookup"><span data-stu-id="ec7a5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ec7a5-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS, \_ представление**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS\_VIEW**</span></span>
</dt> <dd>

<span data-ttu-id="ec7a5-108">Определяет матрицу преобразования, заданную как матрица преобразования представления.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-108">Identifies the transformation matrix being set as the view transformation matrix.</span></span> <span data-ttu-id="ec7a5-109">Значение по умолчанию — **null** (матрица идентификаторов).</span><span class="sxs-lookup"><span data-stu-id="ec7a5-109">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="ec7a5-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**\_ПРОЕКЦИЯ D3DTS**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS\_PROJECTION**</span></span>
</dt> <dd>

<span data-ttu-id="ec7a5-111">Определяет матрицу преобразования, заданную как матрица преобразования проекции.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-111">Identifies the transformation matrix being set as the projection transformation matrix.</span></span> <span data-ttu-id="ec7a5-112">Значение по умолчанию — **null** (матрица идентификаторов).</span><span class="sxs-lookup"><span data-stu-id="ec7a5-112">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="ec7a5-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS\_TEXTURE0**</span></span>
</dt> <dd>

<span data-ttu-id="ec7a5-114">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-114">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec7a5-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ TEXTURE1**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS\_TEXTURE1**</span></span>
</dt> <dd>

<span data-ttu-id="ec7a5-116">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-116">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec7a5-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ TEXTURE2**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS\_TEXTURE2**</span></span>
</dt> <dd>

<span data-ttu-id="ec7a5-118">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-118">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec7a5-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS\_TEXTURE3**</span></span>
</dt> <dd>

<span data-ttu-id="ec7a5-120">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-120">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec7a5-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS\_TEXTURE4**</span></span>
</dt> <dd>

<span data-ttu-id="ec7a5-122">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-122">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec7a5-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS\_TEXTURE5**</span></span>
</dt> <dd>

<span data-ttu-id="ec7a5-124">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-124">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec7a5-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS\_TEXTURE6**</span></span>
</dt> <dd>

<span data-ttu-id="ec7a5-126">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-126">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec7a5-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS\_TEXTURE7**</span></span>
</dt> <dd>

<span data-ttu-id="ec7a5-128">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-128">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="ec7a5-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="ec7a5-130">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-130">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="ec7a5-131">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-131">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="ec7a5-132">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-132">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec7a5-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec7a5-133">Remarks</span></span>

<span data-ttu-id="ec7a5-134">Состояния преобразования в диапазоне от 256 до 511 зарезервированы для хранения до 256 матриц мира, которые можно индексировать с помощью \_ макросов D3DTS ворлдматрикс и D3DTS \_ World.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-134">The transform states in the range 256 through 511 are reserved to store up to 256 world matrices that can be indexed using the D3DTS\_WORLDMATRIX and D3DTS\_WORLD macros.</span></span>



| <span data-ttu-id="ec7a5-135">Макросы</span><span class="sxs-lookup"><span data-stu-id="ec7a5-135">Macros</span></span>                                                  |                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec7a5-136">**D3DTS \_ мир**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-136">**D3DTS\_WORLD**</span></span>](d3dts-world.md)                     | <span data-ttu-id="ec7a5-137">Эквивалентно D3DTS \_ ворлдматрикс (0).</span><span class="sxs-lookup"><span data-stu-id="ec7a5-137">Equivalent to D3DTS\_WORLDMATRIX(0).</span></span>                                                                                                                                  |
| <span data-ttu-id="ec7a5-138">[**D3DTS \_ ВОРЛДМАТРИКС**](d3dts-worldmatrix.md) (индекс)</span><span class="sxs-lookup"><span data-stu-id="ec7a5-138">[**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span></span> | <span data-ttu-id="ec7a5-139">Определяет матрицу преобразования, заданную для матрицы мира по индексу.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-139">Identifies the transform matrix to set for the world matrix at index.</span></span> <span data-ttu-id="ec7a5-140">Несколько мировых матриц используются только для смешивания вершин.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-140">Multiple world matrices are used only for vertex blending.</span></span> <span data-ttu-id="ec7a5-141">В противном случае используется только D3DTS \_ World.</span><span class="sxs-lookup"><span data-stu-id="ec7a5-141">Otherwise only D3DTS\_WORLD is used.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="ec7a5-142">Требования</span><span class="sxs-lookup"><span data-stu-id="ec7a5-142">Requirements</span></span>



| <span data-ttu-id="ec7a5-143">Требование</span><span class="sxs-lookup"><span data-stu-id="ec7a5-143">Requirement</span></span> | <span data-ttu-id="ec7a5-144">Значение</span><span class="sxs-lookup"><span data-stu-id="ec7a5-144">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7a5-145">Header</span><span class="sxs-lookup"><span data-stu-id="ec7a5-145">Header</span></span><br/> | <dl> <span data-ttu-id="ec7a5-146"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec7a5-146"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec7a5-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec7a5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec7a5-148">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="ec7a5-148">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="ec7a5-149">**IDirect3DDevice9:: Transform**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-149">**IDirect3DDevice9::GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="ec7a5-150">**IDirect3DDevice9:: Мултиплитрансформ**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-150">**IDirect3DDevice9::MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="ec7a5-151">**IDirect3DDevice9:: Сеттрансформ**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-151">**IDirect3DDevice9::SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="ec7a5-152">**D3DTS \_ мир**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-152">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="ec7a5-153">**D3DTS \_ ворлдн**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-153">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="ec7a5-154">**D3DTS \_ ворлдматрикс**</span><span class="sxs-lookup"><span data-stu-id="ec7a5-154">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
