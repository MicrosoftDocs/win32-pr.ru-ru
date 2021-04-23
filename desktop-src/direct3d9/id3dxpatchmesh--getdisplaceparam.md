---
description: Возвращает параметры смещения геометрического объекта сетки.
ms.assetid: 155724ba-71be-4e9f-8c84-bb04f8eec578
title: 'Метод ID3DXPatchMesh:: Жетдисплацепарам (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ce6891af8a15aa8f4af5c85312f124db6c05321
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714036"
---
# <a name="id3dxpatchmeshgetdisplaceparam-method"></a><span data-ttu-id="80865-103">Метод ID3DXPatchMesh:: Жетдисплацепарам</span><span class="sxs-lookup"><span data-stu-id="80865-103">ID3DXPatchMesh::GetDisplaceParam method</span></span>

<span data-ttu-id="80865-104">Возвращает параметры смещения геометрического объекта сетки.</span><span class="sxs-lookup"><span data-stu-id="80865-104">Gets mesh geometry displacement parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="80865-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80865-105">Syntax</span></span>


```C++
HRESULT GetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 *Texture,
  [in] D3DTEXTUREFILTERTYPE   *MinFilter,
  [in] D3DTEXTUREFILTERTYPE   *MagFilter,
  [in] D3DTEXTUREFILTERTYPE   *MipFilter,
  [in] D3DTEXTUREADDRESS      *Wrap,
  [in] DWORD                  *dwLODBias
);
```



## <a name="parameters"></a><span data-ttu-id="80865-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80865-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80865-107">*Текстура* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80865-107">*Texture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80865-108">Тип: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="80865-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span></span>

<span data-ttu-id="80865-109">Текстура, содержащая данные смещения.</span><span class="sxs-lookup"><span data-stu-id="80865-109">Texture containing the displacement data.</span></span>

</dd> <dt>

<span data-ttu-id="80865-110">*Минфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80865-110">*MinFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80865-111">Тип: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="80865-111">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="80865-112">Уровень минификации.</span><span class="sxs-lookup"><span data-stu-id="80865-112">Minification level.</span></span> <span data-ttu-id="80865-113">Дополнительные сведения см. в разделе [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="80865-113">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="80865-114">*Магфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80865-114">*MagFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80865-115">Тип: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="80865-115">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="80865-116">Уровень увеличения.</span><span class="sxs-lookup"><span data-stu-id="80865-116">Magnification level.</span></span> <span data-ttu-id="80865-117">Дополнительные сведения см. в разделе [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="80865-117">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="80865-118">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80865-118">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80865-119">Тип: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span><span class="sxs-lookup"><span data-stu-id="80865-119">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***</span></span>

<span data-ttu-id="80865-120">Уровень фильтра MIP.</span><span class="sxs-lookup"><span data-stu-id="80865-120">Mip filter level.</span></span> <span data-ttu-id="80865-121">Дополнительные сведения см. в разделе [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="80865-121">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="80865-122">*Перенос по словам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80865-122">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80865-123">Тип: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***</span><span class="sxs-lookup"><span data-stu-id="80865-123">Type: **[**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***</span></span>

<span data-ttu-id="80865-124">Режим переноса адреса текстуры.</span><span class="sxs-lookup"><span data-stu-id="80865-124">Texture address wrap mode.</span></span> <span data-ttu-id="80865-125">Дополнительные сведения см. в разделе [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="80865-125">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="80865-126">*двлодбиас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="80865-126">*dwLODBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80865-127">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="80865-127">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="80865-128">Уровень детализации значения смещения.</span><span class="sxs-lookup"><span data-stu-id="80865-128">Level of detail bias value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80865-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80865-129">Return value</span></span>

<span data-ttu-id="80865-130">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80865-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80865-131">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="80865-131">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="80865-132">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="80865-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="80865-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80865-133">Remarks</span></span>

<span data-ttu-id="80865-134">Карты смещения могут быть только 2D-текстурой.</span><span class="sxs-lookup"><span data-stu-id="80865-134">Displacement maps can only be 2D textures.</span></span> <span data-ttu-id="80865-135">Функции текстурирования игнорируется для неадаптируемой тесселяции.</span><span class="sxs-lookup"><span data-stu-id="80865-135">Mipmapping is ignored for nonadaptive tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="80865-136">Требования</span><span class="sxs-lookup"><span data-stu-id="80865-136">Requirements</span></span>



| <span data-ttu-id="80865-137">Требование</span><span class="sxs-lookup"><span data-stu-id="80865-137">Requirement</span></span> | <span data-ttu-id="80865-138">Значение</span><span class="sxs-lookup"><span data-stu-id="80865-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80865-139">Header</span><span class="sxs-lookup"><span data-stu-id="80865-139">Header</span></span><br/>  | <dl> <span data-ttu-id="80865-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="80865-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="80865-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80865-141">Library</span></span><br/> | <dl> <span data-ttu-id="80865-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80865-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="80865-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80865-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80865-144">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="80865-144">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
