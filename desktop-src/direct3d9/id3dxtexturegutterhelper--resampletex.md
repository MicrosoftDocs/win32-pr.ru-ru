---
description: Ресамплинг текстуры в гуттерхелпер параметризации.
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: 'Метод ID3DXTextureGutterHelper:: Ресамплетекс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ResampleTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ad8b4cefe0b368cbf81de4ddc030f32cda8fb17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273896"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a><span data-ttu-id="0c1cd-103">Метод ID3DXTextureGutterHelper:: Ресамплетекс</span><span class="sxs-lookup"><span data-stu-id="0c1cd-103">ID3DXTextureGutterHelper::ResampleTex method</span></span>

<span data-ttu-id="0c1cd-104">Ресамплинг текстуры в гуттерхелпер параметризации.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-104">Resamples a texture into this gutterhelper's parameterization.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c1cd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c1cd-105">Syntax</span></span>


```C++
HRESULT ResampleTex(
  [in]  LPDIRECT3DTEXTURE9 pTextureIn,
  [in]  LPD3DXMESH         pMeshIn,
  [in]  D3DDECLUSAGE       Usage,
  [in]  UINT               UsageIndex,
  [out] LPDIRECT3DTEXTURE9 pTextureOut
);
```



## <a name="parameters"></a><span data-ttu-id="0c1cd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c1cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c1cd-107">*птекстуреин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c1cd-107">*pTextureIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c1cd-108">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="0c1cd-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="0c1cd-109">Текстура, соответствующая исходной параметризации в Пмешин.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-109">Texture that corresponds to the original parameterization in pMeshIn.</span></span> <span data-ttu-id="0c1cd-110">Эта текстура будет использоваться для создания Птекстуреаут.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-110">This texture will be used to create pTextureOut.</span></span>

</dd> <dt>

<span data-ttu-id="0c1cd-111">*пмешин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c1cd-111">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c1cd-112">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="0c1cd-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="0c1cd-113">Сетка, содержащая исходную и новую параметризации.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-113">Mesh containing the original and new parameterizations.</span></span> <span data-ttu-id="0c1cd-114">Необходимо сохранить новую параметризацию в D3DDECLUSAGE \_ текскурд с индексом 0.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-114">It is required to store the new parameterization in D3DDECLUSAGE\_TEXCOORD index 0.</span></span>

</dd> <dt>

<span data-ttu-id="0c1cd-115">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c1cd-115">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c1cd-116">Тип: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="0c1cd-116">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="0c1cd-117">Использование данных вершин (используется в сочетании с Усажеиндекс), которое определяет компонент объявления вершины, который содержит исходную параметризацию в Пмешин.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-117">Vertex data usage (used in combination with UsageIndex) which identifies the component of the vertex declaration that contains the original parameterization in pMeshIn.</span></span> <span data-ttu-id="0c1cd-118">См. [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="0c1cd-118">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c1cd-119">*Усажеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c1cd-119">*UsageIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c1cd-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c1cd-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c1cd-121">Отсчитываемый от нуля индекс (используется в сочетании с использованием), который определяет компонент объявления вершины, который содержит исходную параметризацию параметров в Пмешин.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-121">Zero-based index (used in combination with Usage), which identifies the component of the vertex declaration that contains the original parameterization in pMeshIn.</span></span> <span data-ttu-id="0c1cd-122">\_Для новой параметризации требуется сочетание D3DDECLUSAGE текскурд и индекса 0; может использоваться любая другая комбинация использования или индекса.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-122">The combination of D3DDECLUSAGE\_TEXCOORD and index 0 is required for the new parameterization; any other usage/index combination may be used.</span></span>

</dd> <dt>

<span data-ttu-id="0c1cd-123">*птекстуреаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0c1cd-123">*pTextureOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c1cd-124">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="0c1cd-124">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="0c1cd-125">Перевыборка текстуры.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-125">Resampled texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c1cd-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c1cd-126">Return value</span></span>

<span data-ttu-id="0c1cd-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0c1cd-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0c1cd-128">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-128">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0c1cd-129">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-129">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c1cd-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c1cd-130">Remarks</span></span>

<span data-ttu-id="0c1cd-131">Параметризация в случае этой функции представляет собой набор координат текстуры, который сопоставляет треугольники сетки с треугольниками на текстуре.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-131">A parameterization in the case of this function is a set of texture coordinates that maps the triangles of a mesh to the triangles on a texture.</span></span> <span data-ttu-id="0c1cd-132">Новая параметризация — это набор координат текстуры, содержащихся в вспомогательном интерфейсе переплета, а исходная параметризация — это набор координат текстуры, содержащихся во входной сетке.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-132">The new parameterization is the set of texture coordinates contained in the gutter helper interface, and the original parameterization is the set of texture coordinates contained within the input mesh.</span></span>

<span data-ttu-id="0c1cd-133">Предполагается, что координаты текстуры находятся в диапазоне от 0 до 1 включительно, а новая параметризация должна быть объявлена в объявлении вершины в качестве индекса координаты текстуры 0.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-133">It is assumed that texture coordinates are between 0 and 1, inclusive, and the new parameterization must be declared in the vertex declaration as texture coordinate index 0.</span></span> <span data-ttu-id="0c1cd-134">Исходная текстура и текстура с интерполяцией должны иметь одинаковую ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-134">The original texture and the resampled texture must have the same width and height.</span></span>

<span data-ttu-id="0c1cd-135">Например, для подготовки к повторной выборки текстуры:</span><span class="sxs-lookup"><span data-stu-id="0c1cd-135">For example, to prepare for resampling a texture:</span></span>

-   <span data-ttu-id="0c1cd-136">Создайте исходный интерфейс текстуры (Поригиналтекс ниже) с помощью функции, такой как [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="0c1cd-136">Create the original texture interface (pOriginalTex below) using a function like [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span></span>
-   <span data-ttu-id="0c1cd-137">Создайте новый интерфейс текстуры для текстуры с интерполяцией (Пресампледтекс ниже).</span><span class="sxs-lookup"><span data-stu-id="0c1cd-137">Create the new texture interface for the resampled texture (pResampledTex below).</span></span> <span data-ttu-id="0c1cd-138">Размер этой текстуры должен соответствовать размеру (ширине и высоте) вспомогательной текстуры переплета.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-138">The size of this texture must match the size (width and height) of the gutter helper texture.</span></span>
-   <span data-ttu-id="0c1cd-139">Вызовите [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) , чтобы получить новую параметризацию, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="0c1cd-139">Call [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) to obtain the new parameterization as shown here:</span></span>


```
// Given:
// pMesh points to a mesh that contains the original and new texture coordinates
ID3DXTextureGutterHelper * pGutterHelper;
    
// Mesh vertex declaration
D3DVERTEXELEMENT9 decl[] = {
    {0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0},
    // contains new set of texcoords
    {0, 24, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0}, 
    // contains original set of texcoords
    {0, 32, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1}, 
    D3DDECL_END()
};
    
// Create a gutter helper with the new parameterization
hr = D3DXCreateTextureGutterHelper(width, height, pMesh, 1, &pGutterHelper);  
    
// Resample the texture
hr = pGutterHelper->ResampleTex(pOriginalTex, pMesh, D3DDECLUSAGE_TEXCOORD, 
           1, pResampledTex); 
    
// Release the gutter helper interface when done with it
```



<span data-ttu-id="0c1cd-140">Одним из распространенных сценариев может быть использование Уватлас для создания текстуры Atlas и последующее использование Ресамплетекс для повторной выборки текстуры в новой параметризации.</span><span class="sxs-lookup"><span data-stu-id="0c1cd-140">One common scenario might be to use UVAtlas to create a texture atlas and then use ResampleTex to resample the texture into the new parameterization.</span></span> <span data-ttu-id="0c1cd-141">Дополнительные сведения о атласов см. [в разделе Использование уватлас (Direct3D 9)](using-uvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="0c1cd-141">For more information about atlases, see [Using UVAtlas (Direct3D 9)](using-uvatlas.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c1cd-142">Требования</span><span class="sxs-lookup"><span data-stu-id="0c1cd-142">Requirements</span></span>



| <span data-ttu-id="0c1cd-143">Требование</span><span class="sxs-lookup"><span data-stu-id="0c1cd-143">Requirement</span></span> | <span data-ttu-id="0c1cd-144">Значение</span><span class="sxs-lookup"><span data-stu-id="0c1cd-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c1cd-145">Header</span><span class="sxs-lookup"><span data-stu-id="0c1cd-145">Header</span></span><br/>  | <dl> <span data-ttu-id="0c1cd-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c1cd-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0c1cd-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0c1cd-147">Library</span></span><br/> | <dl> <span data-ttu-id="0c1cd-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c1cd-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0c1cd-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c1cd-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c1cd-150">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="0c1cd-150">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> <dt>

[<span data-ttu-id="0c1cd-151">**D3DXUVAtlasCreate**</span><span class="sxs-lookup"><span data-stu-id="0c1cd-151">**D3DXUVAtlasCreate**</span></span>](d3dxuvatlascreate.md)
</dt> </dl>

 

 
