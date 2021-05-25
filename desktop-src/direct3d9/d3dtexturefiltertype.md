---
description: Определяет режимы фильтрации текстур для этапа текстуры.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Перечисление D3DTEXTUREFILTERTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREFILTERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bd6038e1b3d2b2f85e5766605583db9879427343
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343009"
---
# <a name="d3dtexturefiltertype-enumeration"></a><span data-ttu-id="4c769-103">Перечисление D3DTEXTUREFILTERTYPE</span><span class="sxs-lookup"><span data-stu-id="4c769-103">D3DTEXTUREFILTERTYPE enumeration</span></span>

<span data-ttu-id="4c769-104">Определяет режимы фильтрации текстур для этапа текстуры.</span><span class="sxs-lookup"><span data-stu-id="4c769-104">Defines texture filtering modes for a texture stage.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c769-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c769-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREFILTERTYPE { 
  D3DTEXF_NONE             = 0,
  D3DTEXF_POINT            = 1,
  D3DTEXF_LINEAR           = 2,
  D3DTEXF_ANISOTROPIC      = 3,
  D3DTEXF_PYRAMIDALQUAD    = 6,
  D3DTEXF_GAUSSIANQUAD     = 7,
  D3DTEXF_CONVOLUTIONMONO  = 8,
  D3DTEXF_FORCE_DWORD      = 0x7fffffff
} D3DTEXTUREFILTERTYPE, *LPD3DTEXTUREFILTERTYPE;
```



## <a name="constants"></a><span data-ttu-id="4c769-106">Константы</span><span class="sxs-lookup"><span data-stu-id="4c769-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4c769-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ None**</span><span class="sxs-lookup"><span data-stu-id="4c769-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="4c769-108">При использовании с [**D3DSAMP \_ мипфилтер**](./d3dsamplerstatetype.md)отключает функции текстурирования.</span><span class="sxs-lookup"><span data-stu-id="4c769-108">When used with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md), disables mipmapping.</span></span>

</dd> <dt>

<span data-ttu-id="4c769-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**\_Точка D3DTEXF**</span><span class="sxs-lookup"><span data-stu-id="4c769-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="4c769-110">При использовании с [**D3DSAMP \_ Магфилтер**](./d3dsamplerstatetype.md) или [**D3DSAMP \_ минфилтер**](./d3dsamplerstatetype.md)указывает, что фильтрация точек должна использоваться как значение увеличения текстуры или фильтр минификации соответственно.</span><span class="sxs-lookup"><span data-stu-id="4c769-110">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that point filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="4c769-111">При использовании с **D3DSAMP \_ мипфилтер** включает функции текстурирования и указывает, что средство программной прорисовки выбирает цвет из шаг текселя ближайшего уровня MIP.</span><span class="sxs-lookup"><span data-stu-id="4c769-111">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and specifies that the rasterizer chooses the color from the texel of the nearest mip level.</span></span>

</dd> <dt>

<span data-ttu-id="4c769-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**\_Линейная D3DTEXF**</span><span class="sxs-lookup"><span data-stu-id="4c769-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="4c769-113">При использовании с [**D3DSAMP \_ Магфилтер**](./d3dsamplerstatetype.md) или [**D3DSAMP \_ минфилтер**](./d3dsamplerstatetype.md)указывает, что Линейная фильтрация используется в качестве коэффициента увеличения текстуры или фильтра минификации соответственно.</span><span class="sxs-lookup"><span data-stu-id="4c769-113">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that linear filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="4c769-114">При использовании с **D3DSAMP \_ мипфилтер** включает фильтрацию функции текстурирования и трилинейной; она указывает, что средство программной прорисовки выполняет интерполяцию между двумя ближайшими уровнями MIP.</span><span class="sxs-lookup"><span data-stu-id="4c769-114">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and trilinear filtering; it specifies that the rasterizer interpolates between the two nearest mip levels.</span></span>

</dd> <dt>

<span data-ttu-id="4c769-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ анизотропный**</span><span class="sxs-lookup"><span data-stu-id="4c769-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF\_ANISOTROPIC**</span></span>
</dt> <dd>

<span data-ttu-id="4c769-116">При использовании с [**D3DSAMP \_ Магфилтер**](./d3dsamplerstatetype.md) или [**D3DSAMP \_ минфилтер**](./d3dsamplerstatetype.md)указывает, что анизотропная фильтрация текстур используется в качестве фильтра увеличения текстуры или фильтр минификации соответственно.</span><span class="sxs-lookup"><span data-stu-id="4c769-116">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that anisotropic texture filtering used as a texture magnification or minification filter respectively.</span></span> <span data-ttu-id="4c769-117">Компенсирует искажения, вызванные различием угла между многоугольником текстуры и плоскостью экрана.</span><span class="sxs-lookup"><span data-stu-id="4c769-117">Compensates for distortion caused by the difference in angle between the texture polygon and the plane of the screen.</span></span> <span data-ttu-id="4c769-118">Использование WITH **D3DSAMP \_ мипфилтер** не определено.</span><span class="sxs-lookup"><span data-stu-id="4c769-118">Use with **D3DSAMP\_MIPFILTER** is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="4c769-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ пирамидалкуад**</span><span class="sxs-lookup"><span data-stu-id="4c769-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF\_PYRAMIDALQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="4c769-120">4-примерный фильтр, используемый в качестве фильтра увеличения текстуры или минификации.</span><span class="sxs-lookup"><span data-stu-id="4c769-120">A 4-sample tent filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="4c769-121">Использование WITH [**D3DSAMP \_ мипфилтер**](./d3dsamplerstatetype.md) не определено.</span><span class="sxs-lookup"><span data-stu-id="4c769-121">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="4c769-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ гауссианкуад**</span><span class="sxs-lookup"><span data-stu-id="4c769-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF\_GAUSSIANQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="4c769-123">4-примерный фильтр по Гауссу, используемый в качестве фильтра увеличения текстуры или минификации.</span><span class="sxs-lookup"><span data-stu-id="4c769-123">A 4-sample Gaussian filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="4c769-124">Использование WITH [**D3DSAMP \_ мипфилтер**](./d3dsamplerstatetype.md) не определено.</span><span class="sxs-lookup"><span data-stu-id="4c769-124">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="4c769-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ конволутионмоно**</span><span class="sxs-lookup"><span data-stu-id="4c769-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF\_CONVOLUTIONMONO**</span></span>
</dt> <dd>

<span data-ttu-id="4c769-126">Фильтр свертки для монохромных текстур.</span><span class="sxs-lookup"><span data-stu-id="4c769-126">Convolution filter for monochrome textures.</span></span> <span data-ttu-id="4c769-127">См. [D3DFMT \_ a1](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="4c769-127">See [D3DFMT\_A1](d3dformat.md).</span></span>

<span data-ttu-id="4c769-128">Различия между Direct3D 9 и Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="4c769-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="4c769-129">Этот флаг доступен только в Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="4c769-129">This flag is available in Direct3D 9Ex only.</span></span>



 

<span data-ttu-id="4c769-130">Использование WITH [**D3DSAMP \_ мипфилтер**](./d3dsamplerstatetype.md) не определено.</span><span class="sxs-lookup"><span data-stu-id="4c769-130">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="4c769-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4c769-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="4c769-132">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="4c769-132">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="4c769-133">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="4c769-133">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="4c769-134">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="4c769-134">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c769-135">Remarks</span><span class="sxs-lookup"><span data-stu-id="4c769-135">Remarks</span></span>

<span data-ttu-id="4c769-136">D3DTEXTUREFILTERTYPE используется [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) вместе с [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) для определения режимов фильтрации текстур для этапа текстуры.</span><span class="sxs-lookup"><span data-stu-id="4c769-136">D3DTEXTUREFILTERTYPE is used by [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) along with [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) to define texture filtering modes for a texture stage.</span></span>

<span data-ttu-id="4c769-137">Чтобы проверить, поддерживает ли формат типы фильтров текстур, отличные от D3DTEXF \_ Point (которая всегда поддерживается), вызовите [**IDirect3D9:: чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) с \_ \_ фильтром запросов D3DUSAGE.</span><span class="sxs-lookup"><span data-stu-id="4c769-137">To check if a format supports texture filter types other than D3DTEXF\_POINT (which is always supported), call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_FILTER.</span></span>

<span data-ttu-id="4c769-138">Задайте фильтр увеличения масштаба для этапа текстуры, вызвав [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) со значением D3DSAMP \_ магфилтер в качестве второго параметра и одним элементом этого перечисления в качестве третьего.</span><span class="sxs-lookup"><span data-stu-id="4c769-138">Set a texture stage's magnification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MAGFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="4c769-139">Задайте фильтр минификации для этапа текстуры, вызвав [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) со значением D3DSAMP \_ минфилтер в качестве второго параметра и одним членом этого перечисления в качестве третьего параметра.</span><span class="sxs-lookup"><span data-stu-id="4c769-139">Set a texture stage's minification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MINFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="4c769-140">Задайте фильтр текстуры для использования уровней между-mipmap, вызвав [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) со значением D3DSAMP \_ мипфилтер в качестве второго параметра и одним членом этого перечисления в качестве третьего параметра.</span><span class="sxs-lookup"><span data-stu-id="4c769-140">Set the texture filter to use between-mipmap levels by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MIPFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="4c769-141">Не все допустимые режимы фильтрации для устройства будут применяться к картам томов.</span><span class="sxs-lookup"><span data-stu-id="4c769-141">Not all valid filtering modes for a device will apply to volume maps.</span></span> <span data-ttu-id="4c769-142">В общем случае \_ \_ для карт томов будут поддерживаться линейные фильтры увеличения D3DTEXF Point и D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="4c769-142">In general, D3DTEXF\_POINT and D3DTEXF\_LINEAR magnification filters will be supported for volume maps.</span></span> <span data-ttu-id="4c769-143">Если \_ задано значение D3DPTEXTURECAPS мипволумемап, то \_ \_ \_ для карт томов будут поддерживаться фильтры D3DTEXF Point mipmap и D3DTEXF Point и D3DTEXF линейные минификации.</span><span class="sxs-lookup"><span data-stu-id="4c769-143">If D3DPTEXTURECAPS\_MIPVOLUMEMAP is set, then the D3DTEXF\_POINT mipmap filter and D3DTEXF\_POINT and D3DTEXF\_LINEAR minification filters will be supported for volume maps.</span></span> <span data-ttu-id="4c769-144">Устройство может иметь или не поддерживать \_ Фильтр линейного mipmap D3DTEXF для карт томов.</span><span class="sxs-lookup"><span data-stu-id="4c769-144">The device may or may not support the D3DTEXF\_LINEAR mipmap filter for volume maps.</span></span> <span data-ttu-id="4c769-145">Устройства, поддерживающие анизотропную фильтрацию для двумерных карт, не обязательно поддерживают анизотропную фильтрацию для карт томов.</span><span class="sxs-lookup"><span data-stu-id="4c769-145">Devices that support anisotropic filtering for 2D maps do not necessarily support anisotropic filtering for volume maps.</span></span> <span data-ttu-id="4c769-146">Однако приложения, которые включают анизотропную фильтрацию, получат наилучшую доступную фильтрацию (возможно, линейную), если анизотропная фильтрация не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4c769-146">However, applications that enable anisotropic filtering will receive the best available filtering (probably linear) if anisotropic filtering is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c769-147">Требования</span><span class="sxs-lookup"><span data-stu-id="4c769-147">Requirements</span></span>



| <span data-ttu-id="4c769-148">Требование</span><span class="sxs-lookup"><span data-stu-id="4c769-148">Requirement</span></span> | <span data-ttu-id="4c769-149">Значение</span><span class="sxs-lookup"><span data-stu-id="4c769-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c769-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4c769-150">Header</span></span><br/> | <dl> <span data-ttu-id="4c769-151"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c769-151"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c769-152">См. также</span><span class="sxs-lookup"><span data-stu-id="4c769-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c769-153">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="4c769-153">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="4c769-154">**ID3DXPatchMesh:: Жетдисплацепарам**</span><span class="sxs-lookup"><span data-stu-id="4c769-154">**ID3DXPatchMesh::GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="4c769-155">**ID3DXPatchMesh:: Сетдисплацепарам**</span><span class="sxs-lookup"><span data-stu-id="4c769-155">**ID3DXPatchMesh::SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="4c769-156">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="4c769-156">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> <dt>

[<span data-ttu-id="4c769-157">**IDirect3DDevice9::SetSamplerState**</span><span class="sxs-lookup"><span data-stu-id="4c769-157">**IDirect3DDevice9::SetSamplerState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
