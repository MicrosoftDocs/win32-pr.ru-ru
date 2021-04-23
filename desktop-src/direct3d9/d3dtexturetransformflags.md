---
description: Определяет значения преобразования координат текстуры.
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: Перечисление D3DTEXTURETRANSFORMFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 63426c0d57dee02823ee2f37327ba7c66d421b24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273719"
---
# <a name="d3dtexturetransformflags-enumeration"></a><span data-ttu-id="6ffca-103">Перечисление D3DTEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="6ffca-103">D3DTEXTURETRANSFORMFLAGS enumeration</span></span>

<span data-ttu-id="6ffca-104">Определяет значения преобразования координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="6ffca-104">Defines texture coordinate transformation values.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ffca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ffca-105">Syntax</span></span>


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a><span data-ttu-id="6ffca-106">Константы</span><span class="sxs-lookup"><span data-stu-id="6ffca-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6ffca-107"><span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**\_Отключение D3DTTFF**</span><span class="sxs-lookup"><span data-stu-id="6ffca-107"><span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**D3DTTFF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="6ffca-108">Координаты текстуры передаются непосредственно в средство программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="6ffca-108">Texture coordinates are passed directly to the rasterizer.</span></span>

</dd> <dt>

<span data-ttu-id="6ffca-109"><span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF \_ COUNT1**</span><span class="sxs-lookup"><span data-stu-id="6ffca-109"><span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF\_COUNT1**</span></span>
</dt> <dd>

<span data-ttu-id="6ffca-110">Средство программной прорисовки должно рассчитывать Координаты одномерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="6ffca-110">The rasterizer should expect 1D texture coordinates.</span></span> <span data-ttu-id="6ffca-111">Это значение используется при обработке вершин фиксированной функции. При использовании программируемого шейдера вершин для него должно быть задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="6ffca-111">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="6ffca-112"><span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF \_ COUNT2**</span><span class="sxs-lookup"><span data-stu-id="6ffca-112"><span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF\_COUNT2**</span></span>
</dt> <dd>

<span data-ttu-id="6ffca-113">Средство программной прорисовки должно рассчитывать координаты двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="6ffca-113">The rasterizer should expect 2D texture coordinates.</span></span> <span data-ttu-id="6ffca-114">Это значение используется при обработке вершин фиксированной функции. При использовании программируемого шейдера вершин для него должно быть задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="6ffca-114">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="6ffca-115"><span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF \_ COUNT3**</span><span class="sxs-lookup"><span data-stu-id="6ffca-115"><span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF\_COUNT3**</span></span>
</dt> <dd>

<span data-ttu-id="6ffca-116">Средство программной прорисовки должно рассчитывать координаты трехмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="6ffca-116">The rasterizer should expect 3D texture coordinates.</span></span> <span data-ttu-id="6ffca-117">Это значение используется при обработке вершин фиксированной функции. При использовании программируемого шейдера вершин для него должно быть задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="6ffca-117">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="6ffca-118"><span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF \_ COUNT4**</span><span class="sxs-lookup"><span data-stu-id="6ffca-118"><span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF\_COUNT4**</span></span>
</dt> <dd>

<span data-ttu-id="6ffca-119">Средство программной прорисовки должно рассчитывать координаты текстуры 4D.</span><span class="sxs-lookup"><span data-stu-id="6ffca-119">The rasterizer should expect 4D texture coordinates.</span></span> <span data-ttu-id="6ffca-120">Это значение используется при обработке вершин фиксированной функции. При использовании программируемого шейдера вершин для него должно быть задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="6ffca-120">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="6ffca-121"><span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ Прогноз**</span><span class="sxs-lookup"><span data-stu-id="6ffca-121"><span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF\_PROJECTED**</span></span>
</dt> <dd>

<span data-ttu-id="6ffca-122">Этот флаг учитывается с помощью конвейера пикселей функции с фиксированной функцией, а также программируемого конвейера пикселей в версиях PS \_ 1 \_ 1 до PS \_ 1 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="6ffca-122">This flag is honored by the fixed function pixel pipeline, as well as the programmable pixel pipeline in versions ps\_1\_1 to ps\_1\_3.</span></span> <span data-ttu-id="6ffca-123">Если для этапа текстуры включена проекция текстуры, все четыре значения с плавающей запятой должны быть записаны в соответствующий регистр текстуры.</span><span class="sxs-lookup"><span data-stu-id="6ffca-123">When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register.</span></span> <span data-ttu-id="6ffca-124">Каждая координата текстуры делится на последний элемент перед передачей в средство программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="6ffca-124">Each texture coordinate is divided by the last element before being passed to the rasterizer.</span></span> <span data-ttu-id="6ffca-125">Например, если этот флаг указан с \_ флагом D3DTTFF COUNT3, то первая и вторая координаты текстуры делятся на третью координат перед передачей в средство программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="6ffca-125">For example, if this flag is specified with the D3DTTFF\_COUNT3 flag, the first and second texture coordinates are divided by the third coordinate before being passed to the rasterizer.</span></span>

</dd> <dt>

<span data-ttu-id="6ffca-126"><span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6ffca-126"><span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="6ffca-127">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="6ffca-127">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="6ffca-128">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="6ffca-128">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="6ffca-129">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="6ffca-129">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ffca-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ffca-130">Remarks</span></span>

<span data-ttu-id="6ffca-131">Координаты текстуры можно преобразовать с помощью матрицы размером 4 x 4 до передачи результатов в средство программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="6ffca-131">Texture coordinates can be transformed using a 4 x 4 matrix before the results are passed to the rasterizer.</span></span> <span data-ttu-id="6ffca-132">Преобразования координат текстуры задаются путем вызова [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/desktop/api)и передачи в \_ состояние этапа текстуры D3DTSS текстуретрансформфлагс и одного из значений из **D3DTEXTURETRANSFORMFLAGS**.</span><span class="sxs-lookup"><span data-stu-id="6ffca-132">The texture coordinate transforms are set by calling [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api), and by passing in the D3DTSS\_TEXTURETRANSFORMFLAGS texture stage state and one of the values from **D3DTEXTURETRANSFORMFLAGS**.</span></span> <span data-ttu-id="6ffca-133">Дополнительные сведения о преобразованиях текстур см. в разделе [преобразования координат текстуры (Direct3D 9)](texture-coordinate-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="6ffca-133">For more information about texture transforms, see [Texture Coordinate Transformations (Direct3D 9)](texture-coordinate-transformations.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ffca-134">Требования</span><span class="sxs-lookup"><span data-stu-id="6ffca-134">Requirements</span></span>



| <span data-ttu-id="6ffca-135">Требование</span><span class="sxs-lookup"><span data-stu-id="6ffca-135">Requirement</span></span> | <span data-ttu-id="6ffca-136">Значение</span><span class="sxs-lookup"><span data-stu-id="6ffca-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffca-137">Header</span><span class="sxs-lookup"><span data-stu-id="6ffca-137">Header</span></span><br/> | <dl> <span data-ttu-id="6ffca-138"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ffca-138"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ffca-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ffca-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ffca-140">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="6ffca-140">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="6ffca-141">**D3DTEXTURESTAGESTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="6ffca-141">**D3DTEXTURESTAGESTATETYPE**</span></span>](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
