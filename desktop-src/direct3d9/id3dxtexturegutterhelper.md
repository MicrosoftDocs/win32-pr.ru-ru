---
description: Интерфейс ID3DXTextureGutterHelper используется для создания областей переплета и управления ими в текстуре. Области переплета разделяют текстуры и позволяют билинейной интерполяцию, чтобы избежать артефактов отрисовки на границах текстур.
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: Интерфейс ID3DXTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ece03e14da490bd6d6f5aef69f9457939bc8bab7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355613"
---
# <a name="id3dxtexturegutterhelper-interface"></a><span data-ttu-id="bd027-104">Интерфейс ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="bd027-104">ID3DXTextureGutterHelper interface</span></span>

<span data-ttu-id="bd027-105">Интерфейс ID3DXTextureGutterHelper используется для создания областей переплета и управления ими в текстуре.</span><span class="sxs-lookup"><span data-stu-id="bd027-105">The ID3DXTextureGutterHelper interface is used to build and manage gutter regions in a texture.</span></span> <span data-ttu-id="bd027-106">Области переплета разделяют текстуры и позволяют билинейной интерполяцию, чтобы избежать артефактов отрисовки на границах текстур.</span><span class="sxs-lookup"><span data-stu-id="bd027-106">Gutter regions separate textures and allow for bilinear interpolation to avoid rendering artifacts at texture boundaries.</span></span>

<span data-ttu-id="bd027-107">Получение... методы предоставляют доступ к структурам данных, используемым функцией Apply... метод.</span><span class="sxs-lookup"><span data-stu-id="bd027-107">The Get... methods provide access to the data structures used by the Apply... methods.</span></span>

## <a name="members"></a><span data-ttu-id="bd027-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="bd027-108">Members</span></span>

<span data-ttu-id="bd027-109">Интерфейс **ID3DXTextureGutterHelper** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bd027-109">The **ID3DXTextureGutterHelper** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bd027-110">**ID3DXTextureGutterHelper** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bd027-110">**ID3DXTextureGutterHelper** also has these types of members:</span></span>

-   [<span data-ttu-id="bd027-111">Методы</span><span class="sxs-lookup"><span data-stu-id="bd027-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bd027-112">Методы</span><span class="sxs-lookup"><span data-stu-id="bd027-112">Methods</span></span>

<span data-ttu-id="bd027-113">Интерфейс **ID3DXTextureGutterHelper** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="bd027-113">The **ID3DXTextureGutterHelper** interface has these methods.</span></span>



| <span data-ttu-id="bd027-114">Метод</span><span class="sxs-lookup"><span data-stu-id="bd027-114">Method</span></span>                                                                   | <span data-ttu-id="bd027-115">Описание</span><span class="sxs-lookup"><span data-stu-id="bd027-115">Description</span></span>                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd027-116">**апплигуттерсфлоат**</span><span class="sxs-lookup"><span data-stu-id="bd027-116">**ApplyGuttersFloat**</span></span>](id3dxtexturegutterhelper--applyguttersfloat.md) | <span data-ttu-id="bd027-117">Применяет переплет к буферу текстуры с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="bd027-117">Applies gutters to a FLOAT texture buffer.</span></span><br/>                                                  |
| [<span data-ttu-id="bd027-118">**апплигуттерспрт**</span><span class="sxs-lookup"><span data-stu-id="bd027-118">**ApplyGuttersPRT**</span></span>](id3dxtexturegutterhelper--applyguttersprt.md)     | <span data-ttu-id="bd027-119">Применяет переплет к объекту [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span><span class="sxs-lookup"><span data-stu-id="bd027-119">Applies gutters to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer object.</span></span><br/>               |
| [<span data-ttu-id="bd027-120">**апплигуттерстекс**</span><span class="sxs-lookup"><span data-stu-id="bd027-120">**ApplyGuttersTex**</span></span>](id3dxtexturegutterhelper--applygutterstex.md)     | <span data-ttu-id="bd027-121">Применяет переплет к объекту текстуры [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="bd027-121">Applies gutters to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object.</span></span><br/>        |
| [<span data-ttu-id="bd027-122">**жетбаримап**</span><span class="sxs-lookup"><span data-stu-id="bd027-122">**GetBaryMap**</span></span>](id3dxtexturegutterhelper--getbarymap.md)               | <span data-ttu-id="bd027-123">Получает координаты шаг текселя барицентрик.</span><span class="sxs-lookup"><span data-stu-id="bd027-123">Retrieves texel barycentric coordinates.</span></span><br/>                                                    |
| [<span data-ttu-id="bd027-124">**жетфацемап**</span><span class="sxs-lookup"><span data-stu-id="bd027-124">**GetFaceMap**</span></span>](id3dxtexturegutterhelper--getfacemap.md)               | <span data-ttu-id="bd027-125">Извлекает индекс грани сетки, к которой принадлежит каждый шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="bd027-125">Retrieves the index of the mesh face to which each texel belongs.</span></span><br/>                           |
| [<span data-ttu-id="bd027-126">**жетгуттермап**</span><span class="sxs-lookup"><span data-stu-id="bd027-126">**GetGutterMap**</span></span>](id3dxtexturegutterhelper--getguttermap.md)           | <span data-ttu-id="bd027-127">Получает значение класса шаг текселя, которое указывает класс шаг текселя в соответствии с расположением каждого шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="bd027-127">Receives a texel class value that indicates texel class according to each texel's location.</span></span><br/> |
| [<span data-ttu-id="bd027-128">**Высота**</span><span class="sxs-lookup"><span data-stu-id="bd027-128">**GetHeight**</span></span>](id3dxtexturegutterhelper--getheight.md)                 | <span data-ttu-id="bd027-129">Получает высоту текстуры в пикселях.</span><span class="sxs-lookup"><span data-stu-id="bd027-129">Retrieves the height of the texture, in pixels.</span></span><br/>                                             |
| [<span data-ttu-id="bd027-130">**жеттекселмап**</span><span class="sxs-lookup"><span data-stu-id="bd027-130">**GetTexelMap**</span></span>](id3dxtexturegutterhelper--gettexelmap.md)             | <span data-ttu-id="bd027-131">Извлекает координаты текстуры (u, v) каждого шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="bd027-131">Retrieves the (u, v) texture coordinates of each texel.</span></span><br/>                                     |
| [<span data-ttu-id="bd027-132">**Полуширинные**</span><span class="sxs-lookup"><span data-stu-id="bd027-132">**GetWidth**</span></span>](id3dxtexturegutterhelper--getwidth.md)                   | <span data-ttu-id="bd027-133">Получает ширину текстуры в пикселях.</span><span class="sxs-lookup"><span data-stu-id="bd027-133">Retrieves the width of the texture, in pixels.</span></span><br/>                                              |
| [<span data-ttu-id="bd027-134">**ресамплетекс**</span><span class="sxs-lookup"><span data-stu-id="bd027-134">**ResampleTex**</span></span>](id3dxtexturegutterhelper--resampletex.md)             | <span data-ttu-id="bd027-135">Ресамплинг текстуры в гуттерхелпер параметризации.</span><span class="sxs-lookup"><span data-stu-id="bd027-135">Resamples a texture into this gutterhelper's parameterization.</span></span><br/>                              |
| [<span data-ttu-id="bd027-136">**сетбаримап**</span><span class="sxs-lookup"><span data-stu-id="bd027-136">**SetBaryMap**</span></span>](id3dxtexturegutterhelper--setbarymap.md)               | <span data-ttu-id="bd027-137">Задает координаты шаг текселя барицентрик.</span><span class="sxs-lookup"><span data-stu-id="bd027-137">Sets texel barycentric coordinates.</span></span><br/>                                                         |
| [<span data-ttu-id="bd027-138">**сетфацемап**</span><span class="sxs-lookup"><span data-stu-id="bd027-138">**SetFaceMap**</span></span>](id3dxtexturegutterhelper--setfacemap.md)               | <span data-ttu-id="bd027-139">Задает индекс грани сетки, к которой принадлежит каждый шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="bd027-139">Sets the index of the mesh face to which each texel belongs.</span></span><br/>                                |
| [<span data-ttu-id="bd027-140">**сетгуттермап**</span><span class="sxs-lookup"><span data-stu-id="bd027-140">**SetGutterMap**</span></span>](id3dxtexturegutterhelper--setguttermap.md)           | <span data-ttu-id="bd027-141">Задает значение класса шаг текселя, указывающее класс шаг текселя в соответствии с расположением каждого шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="bd027-141">Sets a texel class value that indicates texel class according to each texel's location.</span></span><br/>     |
| [<span data-ttu-id="bd027-142">**сеттекселмап**</span><span class="sxs-lookup"><span data-stu-id="bd027-142">**SetTexelMap**</span></span>](id3dxtexturegutterhelper--settexelmap.md)             | <span data-ttu-id="bd027-143">Задает координаты текстуры (u, v) каждого шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="bd027-143">Sets the (u, v) texture coordinates of each texel.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="bd027-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd027-144">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bd027-145">При использовании с предварительно вычисленным радианценым переносом (PRT) Этот интерфейс требует уникальной параметризации модели.</span><span class="sxs-lookup"><span data-stu-id="bd027-145">When used with precomputed radiance transfer (PRT), this interface requires a unique parameterization of the model.</span></span> <span data-ttu-id="bd027-146">Каждый шаг текселя должен соответствовать одной точке на поверхности модели и наоборот.</span><span class="sxs-lookup"><span data-stu-id="bd027-146">Every texel must correspond to a single point on the surface of the model and vice-versa.</span></span> <span data-ttu-id="bd027-147">Если модель включает несколько текстур, ее необходимо разделить на отдельные части, каждая из которых содержит один вспомогательный объект для каждой текстуры.</span><span class="sxs-lookup"><span data-stu-id="bd027-147">If the model includes multiple textures, it must be split into separate pieces that each contain one gutter helper object per texture.</span></span>

 

<span data-ttu-id="bd027-148">Этот интерфейс можно использовать для создания карты в пространстве текстуры, в которой каждый шаг текселя находится в одном из четырех классов.</span><span class="sxs-lookup"><span data-stu-id="bd027-148">This interface can be used to generate a map in texture space in which each texel is in one of four classes.</span></span>



| <span data-ttu-id="bd027-149">Класс шаг текселя</span><span class="sxs-lookup"><span data-stu-id="bd027-149">Texel Class</span></span> | <span data-ttu-id="bd027-150">Расположение шаг текселя</span><span class="sxs-lookup"><span data-stu-id="bd027-150">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd027-151">0</span><span class="sxs-lookup"><span data-stu-id="bd027-151">0</span></span>           | <span data-ttu-id="bd027-152">Недопустимая точка; шаг текселя не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="bd027-152">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="bd027-153">1</span><span class="sxs-lookup"><span data-stu-id="bd027-153">1</span></span>           | <span data-ttu-id="bd027-154">Внутри треугольника.</span><span class="sxs-lookup"><span data-stu-id="bd027-154">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="bd027-155">2</span><span class="sxs-lookup"><span data-stu-id="bd027-155">2</span></span>           | <span data-ttu-id="bd027-156">Внутренняя часть.</span><span class="sxs-lookup"><span data-stu-id="bd027-156">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="bd027-157">4</span><span class="sxs-lookup"><span data-stu-id="bd027-157">4</span></span>           | <span data-ttu-id="bd027-158">Внутреннее внутреннее поле; шаг текселя будет оцениваться как полный пример в методах [**ID3DXTextureGutterHelper:: апплигуттерсфлоат**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: апплигуттерстекс**](id3dxtexturegutterhelper--applygutterstex.md)или [**ID3DXTextureGutterHelper:: апплигуттерспрт**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="bd027-158">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

<span data-ttu-id="bd027-159">Для классов 1 и 2 шаг текселя хранится с лицевой стороны, а также с координатами барицентрик первых двух вершин этого лица.</span><span class="sxs-lookup"><span data-stu-id="bd027-159">For classes 1 and 2, a texel is stored with the face it belongs to, along with barycentric coordinates of the first two vertices of that face.</span></span> <span data-ttu-id="bd027-160">Вершины переплета назначаются ближайшей границе в пространстве текстуры.</span><span class="sxs-lookup"><span data-stu-id="bd027-160">Gutter vertices are assigned to the closest edge in texture space.</span></span>

<span data-ttu-id="bd027-161">Отсутствует класс шаг текселя 3.</span><span class="sxs-lookup"><span data-stu-id="bd027-161">There is no texel class 3.</span></span>

<span data-ttu-id="bd027-162">Интерфейс **ID3DXTextureGutterHelper** получается путем вызова функции [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="bd027-162">The **ID3DXTextureGutterHelper** interface is obtained by calling the [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) function.</span></span>

<span data-ttu-id="bd027-163">Тип LPD3DXTEXTUREGUTTERHELPER определяется как указатель на интерфейс **ID3DXTextureGutterHelper** .</span><span class="sxs-lookup"><span data-stu-id="bd027-163">The LPD3DXTEXTUREGUTTERHELPER type is defined as a pointer to the **ID3DXTextureGutterHelper** interface.</span></span>


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a><span data-ttu-id="bd027-164">Требования</span><span class="sxs-lookup"><span data-stu-id="bd027-164">Requirements</span></span>



| <span data-ttu-id="bd027-165">Требование</span><span class="sxs-lookup"><span data-stu-id="bd027-165">Requirement</span></span> | <span data-ttu-id="bd027-166">Значение</span><span class="sxs-lookup"><span data-stu-id="bd027-166">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd027-167">Header</span><span class="sxs-lookup"><span data-stu-id="bd027-167">Header</span></span><br/>  | <dl> <span data-ttu-id="bd027-168"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd027-168"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bd027-169">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bd027-169">Library</span></span><br/> | <dl> <span data-ttu-id="bd027-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd027-170"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bd027-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd027-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd027-172">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="bd027-172">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
