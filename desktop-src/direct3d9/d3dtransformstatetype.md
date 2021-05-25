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
ms.openlocfilehash: 022aa20fab0739b32aa75eb5f4bc575c0a8ad853
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342999"
---
# <a name="d3dtransformstatetype-enumeration"></a><span data-ttu-id="c8389-103">Перечисление D3DTRANSFORMSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="c8389-103">D3DTRANSFORMSTATETYPE enumeration</span></span>

<span data-ttu-id="c8389-104">Определяет константы, описывающие значения состояния преобразования.</span><span class="sxs-lookup"><span data-stu-id="c8389-104">Defines constants that describe transformation state values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8389-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8389-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="c8389-106">Константы</span><span class="sxs-lookup"><span data-stu-id="c8389-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c8389-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS, \_ представление**</span><span class="sxs-lookup"><span data-stu-id="c8389-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS\_VIEW**</span></span>
</dt> <dd>

<span data-ttu-id="c8389-108">Определяет матрицу преобразования, заданную как матрица преобразования представления.</span><span class="sxs-lookup"><span data-stu-id="c8389-108">Identifies the transformation matrix being set as the view transformation matrix.</span></span> <span data-ttu-id="c8389-109">Значение по умолчанию — **null** (матрица идентификаторов).</span><span class="sxs-lookup"><span data-stu-id="c8389-109">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="c8389-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**\_ПРОЕКЦИЯ D3DTS**</span><span class="sxs-lookup"><span data-stu-id="c8389-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS\_PROJECTION**</span></span>
</dt> <dd>

<span data-ttu-id="c8389-111">Определяет матрицу преобразования, заданную как матрица преобразования проекции.</span><span class="sxs-lookup"><span data-stu-id="c8389-111">Identifies the transformation matrix being set as the projection transformation matrix.</span></span> <span data-ttu-id="c8389-112">Значение по умолчанию — **null** (матрица идентификаторов).</span><span class="sxs-lookup"><span data-stu-id="c8389-112">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="c8389-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**</span><span class="sxs-lookup"><span data-stu-id="c8389-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS\_TEXTURE0**</span></span>
</dt> <dd>

<span data-ttu-id="c8389-114">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="c8389-114">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="c8389-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ TEXTURE1**</span><span class="sxs-lookup"><span data-stu-id="c8389-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS\_TEXTURE1**</span></span>
</dt> <dd>

<span data-ttu-id="c8389-116">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="c8389-116">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="c8389-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ TEXTURE2**</span><span class="sxs-lookup"><span data-stu-id="c8389-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS\_TEXTURE2**</span></span>
</dt> <dd>

<span data-ttu-id="c8389-118">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="c8389-118">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="c8389-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**</span><span class="sxs-lookup"><span data-stu-id="c8389-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS\_TEXTURE3**</span></span>
</dt> <dd>

<span data-ttu-id="c8389-120">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="c8389-120">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="c8389-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**</span><span class="sxs-lookup"><span data-stu-id="c8389-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS\_TEXTURE4**</span></span>
</dt> <dd>

<span data-ttu-id="c8389-122">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="c8389-122">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="c8389-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**</span><span class="sxs-lookup"><span data-stu-id="c8389-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS\_TEXTURE5**</span></span>
</dt> <dd>

<span data-ttu-id="c8389-124">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="c8389-124">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="c8389-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**</span><span class="sxs-lookup"><span data-stu-id="c8389-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS\_TEXTURE6**</span></span>
</dt> <dd>

<span data-ttu-id="c8389-126">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="c8389-126">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="c8389-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**</span><span class="sxs-lookup"><span data-stu-id="c8389-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS\_TEXTURE7**</span></span>
</dt> <dd>

<span data-ttu-id="c8389-128">Определяет матрицу преобразования, заданную для указанной стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="c8389-128">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="c8389-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c8389-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c8389-130">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="c8389-130">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c8389-131">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="c8389-131">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c8389-132">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="c8389-132">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8389-133">Remarks</span><span class="sxs-lookup"><span data-stu-id="c8389-133">Remarks</span></span>

<span data-ttu-id="c8389-134">Состояния преобразования в диапазоне от 256 до 511 зарезервированы для хранения до 256 матриц мира, которые можно индексировать с помощью \_ макросов D3DTS ворлдматрикс и D3DTS \_ World.</span><span class="sxs-lookup"><span data-stu-id="c8389-134">The transform states in the range 256 through 511 are reserved to store up to 256 world matrices that can be indexed using the D3DTS\_WORLDMATRIX and D3DTS\_WORLD macros.</span></span>



| <span data-ttu-id="c8389-135">Макросы</span><span class="sxs-lookup"><span data-stu-id="c8389-135">Macros</span></span>                                                  | <span data-ttu-id="c8389-136">Описание</span><span class="sxs-lookup"><span data-stu-id="c8389-136">Description</span></span>                                                                                                                                                                      |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8389-137">**D3DTS \_ мир**</span><span class="sxs-lookup"><span data-stu-id="c8389-137">**D3DTS\_WORLD**</span></span>](d3dts-world.md)                     | <span data-ttu-id="c8389-138">Эквивалентно D3DTS \_ ворлдматрикс (0).</span><span class="sxs-lookup"><span data-stu-id="c8389-138">Equivalent to D3DTS\_WORLDMATRIX(0).</span></span>                                                                                                                                  |
| <span data-ttu-id="c8389-139">[**D3DTS \_ ВОРЛДМАТРИКС**](d3dts-worldmatrix.md) (индекс)</span><span class="sxs-lookup"><span data-stu-id="c8389-139">[**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span></span> | <span data-ttu-id="c8389-140">Определяет матрицу преобразования, заданную для матрицы мира по индексу.</span><span class="sxs-lookup"><span data-stu-id="c8389-140">Identifies the transform matrix to set for the world matrix at index.</span></span> <span data-ttu-id="c8389-141">Несколько мировых матриц используются только для смешивания вершин.</span><span class="sxs-lookup"><span data-stu-id="c8389-141">Multiple world matrices are used only for vertex blending.</span></span> <span data-ttu-id="c8389-142">В противном случае используется только D3DTS \_ World.</span><span class="sxs-lookup"><span data-stu-id="c8389-142">Otherwise only D3DTS\_WORLD is used.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c8389-143">Требования</span><span class="sxs-lookup"><span data-stu-id="c8389-143">Requirements</span></span>



| <span data-ttu-id="c8389-144">Требование</span><span class="sxs-lookup"><span data-stu-id="c8389-144">Requirement</span></span> | <span data-ttu-id="c8389-145">Значение</span><span class="sxs-lookup"><span data-stu-id="c8389-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8389-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c8389-146">Header</span></span><br/> | <dl> <span data-ttu-id="c8389-147"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8389-147"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8389-148">См. также</span><span class="sxs-lookup"><span data-stu-id="c8389-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8389-149">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="c8389-149">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="c8389-150">**IDirect3DDevice9:: Transform**</span><span class="sxs-lookup"><span data-stu-id="c8389-150">**IDirect3DDevice9::GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="c8389-151">**IDirect3DDevice9:: Мултиплитрансформ**</span><span class="sxs-lookup"><span data-stu-id="c8389-151">**IDirect3DDevice9::MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="c8389-152">**IDirect3DDevice9:: Сеттрансформ**</span><span class="sxs-lookup"><span data-stu-id="c8389-152">**IDirect3DDevice9::SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="c8389-153">**D3DTS \_ мир**</span><span class="sxs-lookup"><span data-stu-id="c8389-153">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="c8389-154">**D3DTS \_ ворлдн**</span><span class="sxs-lookup"><span data-stu-id="c8389-154">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="c8389-155">**D3DTS \_ ворлдматрикс**</span><span class="sxs-lookup"><span data-stu-id="c8389-155">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
