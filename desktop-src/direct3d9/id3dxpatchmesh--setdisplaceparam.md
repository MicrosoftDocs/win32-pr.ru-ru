---
description: Задает параметры смещения геометрических объектов сетки.
ms.assetid: 4c78e5b3-fb63-4341-a811-5531cf9564e7
title: 'Метод ID3DXPatchMesh:: Сетдисплацепарам (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.SetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1d59791859e0330415512db1551709729455d0d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664986"
---
# <a name="id3dxpatchmeshsetdisplaceparam-method"></a><span data-ttu-id="9f749-103">Метод ID3DXPatchMesh:: Сетдисплацепарам</span><span class="sxs-lookup"><span data-stu-id="9f749-103">ID3DXPatchMesh::SetDisplaceParam method</span></span>

<span data-ttu-id="9f749-104">Задает параметры смещения геометрических объектов сетки.</span><span class="sxs-lookup"><span data-stu-id="9f749-104">Sets mesh geometry displacement parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f749-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f749-105">Syntax</span></span>


```C++
HRESULT SetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 Texture,
  [in] D3DTEXTUREFILTERTYPE   MinFilter,
  [in] D3DTEXTUREFILTERTYPE   MagFilter,
  [in] D3DTEXTUREFILTERTYPE   MipFilter,
  [in] D3DTEXTUREADDRESS      Wrap,
  [in] DWORD                  dwLODBias
);
```



## <a name="parameters"></a><span data-ttu-id="9f749-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f749-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f749-107">*Текстура* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f749-107">*Texture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f749-108">Тип: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="9f749-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="9f749-109">Текстура, содержащая данные смещения.</span><span class="sxs-lookup"><span data-stu-id="9f749-109">Texture containing the displacement data.</span></span>

</dd> <dt>

<span data-ttu-id="9f749-110">*Минфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f749-110">*MinFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f749-111">Тип: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span><span class="sxs-lookup"><span data-stu-id="9f749-111">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span></span>

<span data-ttu-id="9f749-112">Уровень минификации.</span><span class="sxs-lookup"><span data-stu-id="9f749-112">Minification level.</span></span> <span data-ttu-id="9f749-113">Дополнительные сведения см. в разделе [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="9f749-113">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f749-114">*Магфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f749-114">*MagFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f749-115">Тип: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span><span class="sxs-lookup"><span data-stu-id="9f749-115">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span></span>

<span data-ttu-id="9f749-116">Уровень увеличения.</span><span class="sxs-lookup"><span data-stu-id="9f749-116">Magnification level.</span></span> <span data-ttu-id="9f749-117">Дополнительные сведения см. в разделе [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="9f749-117">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f749-118">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f749-118">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f749-119">Тип: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span><span class="sxs-lookup"><span data-stu-id="9f749-119">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span></span>

<span data-ttu-id="9f749-120">Уровень фильтра MIP.</span><span class="sxs-lookup"><span data-stu-id="9f749-120">Mip filter level.</span></span> <span data-ttu-id="9f749-121">Дополнительные сведения см. в разделе [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="9f749-121">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f749-122">*Перенос по словам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f749-122">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f749-123">Тип: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)**</span><span class="sxs-lookup"><span data-stu-id="9f749-123">Type: **[**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)**</span></span>

<span data-ttu-id="9f749-124">Режим переноса адреса текстуры.</span><span class="sxs-lookup"><span data-stu-id="9f749-124">Texture address wrap mode.</span></span> <span data-ttu-id="9f749-125">Дополнительные сведения см. в разделе [ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)</span><span class="sxs-lookup"><span data-stu-id="9f749-125">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)</span></span>

</dd> <dt>

<span data-ttu-id="9f749-126">*двлодбиас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f749-126">*dwLODBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f749-127">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f749-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f749-128">Уровень детализации значения смещения.</span><span class="sxs-lookup"><span data-stu-id="9f749-128">Level of detail bias value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f749-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f749-129">Return value</span></span>

<span data-ttu-id="9f749-130">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9f749-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9f749-131">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9f749-131">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9f749-132">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9f749-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f749-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f749-133">Remarks</span></span>

<span data-ttu-id="9f749-134">Карты смещения могут быть только 2D-текстурой.</span><span class="sxs-lookup"><span data-stu-id="9f749-134">Displacement maps can only be 2D textures.</span></span> <span data-ttu-id="9f749-135">Функции текстурирования игнорируется для неадаптируемой тесселяции.</span><span class="sxs-lookup"><span data-stu-id="9f749-135">Mipmapping is ignored for nonadaptive tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f749-136">Требования</span><span class="sxs-lookup"><span data-stu-id="9f749-136">Requirements</span></span>



| <span data-ttu-id="9f749-137">Требование</span><span class="sxs-lookup"><span data-stu-id="9f749-137">Requirement</span></span> | <span data-ttu-id="9f749-138">Значение</span><span class="sxs-lookup"><span data-stu-id="9f749-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f749-139">Header</span><span class="sxs-lookup"><span data-stu-id="9f749-139">Header</span></span><br/>  | <dl> <span data-ttu-id="9f749-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f749-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9f749-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f749-141">Library</span></span><br/> | <dl> <span data-ttu-id="9f749-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f749-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9f749-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f749-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f749-144">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="9f749-144">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
