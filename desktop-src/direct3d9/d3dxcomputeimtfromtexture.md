---
description: Вычисляет ИМТ для каждого треугольника из текстуры, сопоставленной с сеткой, которая может использоваться в качестве входных данных для функций Уватлас D3DX.
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: Функция D3DXComputeIMTFromTexture (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fbed0411f3562e3a05ec2ec4df99dfad6d8c902
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081914"
---
# <a name="d3dxcomputeimtfromtexture-function"></a><span data-ttu-id="41cb3-103">Функция D3DXComputeIMTFromTexture</span><span class="sxs-lookup"><span data-stu-id="41cb3-103">D3DXComputeIMTFromTexture function</span></span>

<span data-ttu-id="41cb3-104">Вычисляет ИМТ для каждого треугольника из текстуры, сопоставленной с сеткой, которая может использоваться в качестве входных данных для [функций УВАТЛАС](dx9-graphics-reference-d3dx-functions-uvatlas.md)D3DX.</span><span class="sxs-lookup"><span data-stu-id="41cb3-104">Calculates per-triangle IMT's from a texture mapped onto a mesh, to be used optionally as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="41cb3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41cb3-105">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="41cb3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="41cb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41cb3-107">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41cb3-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41cb3-108">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="41cb3-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="41cb3-109">Указатель на входную сетку (см. [**ID3DXMesh**](id3dxmesh.md)), которая содержит объект Geometry для вычисления ИМТ.</span><span class="sxs-lookup"><span data-stu-id="41cb3-109">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="41cb3-110">*птекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41cb3-110">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41cb3-111">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="41cb3-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="41cb3-112">Указатель на текстуру (см. [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)), сопоставленный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="41cb3-112">A pointer to the texture (see [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) that is mapped to the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="41cb3-113">*двтекстуреиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41cb3-113">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41cb3-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41cb3-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41cb3-115">Отсчитываемый от нуля индекс координаты текстуры, определяющий, какой набор координат текстуры использовать.</span><span class="sxs-lookup"><span data-stu-id="41cb3-115">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="41cb3-116">*двоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41cb3-116">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41cb3-117">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41cb3-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41cb3-118">Параметры переноса текстур.</span><span class="sxs-lookup"><span data-stu-id="41cb3-118">Texture wrap options.</span></span> <span data-ttu-id="41cb3-119">Это сочетание одного или нескольких [**флагов D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="41cb3-119">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="41cb3-120">*пстатускаллбакк*</span><span class="sxs-lookup"><span data-stu-id="41cb3-120">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="41cb3-121">Тип: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="41cb3-121">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="41cb3-122">Указатель на функцию обратного вызова, чтобы отслеживать ход выполнения вычисления ИМТ.</span><span class="sxs-lookup"><span data-stu-id="41cb3-122">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="41cb3-123">*пусерконтекст*</span><span class="sxs-lookup"><span data-stu-id="41cb3-123">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="41cb3-124">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41cb3-124">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41cb3-125">Указатель на определяемую пользователем переменную, которая передается функции обратного вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="41cb3-125">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="41cb3-126">Обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="41cb3-126">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="41cb3-127">*ппимтдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="41cb3-127">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41cb3-128">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="41cb3-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="41cb3-129">Указатель на буфер (см. [**ID3DXBuffer**](id3dxbuffer.md)), содержащий возвращенный массив ИМТ.</span><span class="sxs-lookup"><span data-stu-id="41cb3-129">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="41cb3-130">Этот массив может быть предоставлен в качестве входных данных для [функций D3DX уватлас](dx9-graphics-reference-d3dx-functions-uvatlas.md) , чтобы определить приоритет распределения пространства текстуры в параметризации текстуры.</span><span class="sxs-lookup"><span data-stu-id="41cb3-130">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41cb3-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41cb3-131">Return value</span></span>

<span data-ttu-id="41cb3-132">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="41cb3-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="41cb3-133">Если функция выполнена успешно, возвращается значение D3D \_ ОК. в противном случае — значение D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="41cb3-133">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="41cb3-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41cb3-134">Remarks</span></span>

<span data-ttu-id="41cb3-135">Учитывая текстуру, которая сопоставляется с поверхностью сетки, алгоритм рассчитывает ИМТ для каждой грани.</span><span class="sxs-lookup"><span data-stu-id="41cb3-135">Given a texture that maps over the surface of the mesh, the algorithm computes the IMT for each face.</span></span> <span data-ttu-id="41cb3-136">Это приведет к тому, что треугольники, содержащие данные сигнала с более низкой частотой, будут занимать меньше пространства в окончательной текстуре Atlas при параметризации с помощью функций Уватлас.</span><span class="sxs-lookup"><span data-stu-id="41cb3-136">This will cause triangles containing lower-frequency signal data to take up less space in the final texture atlas when parameterized with the UVAtlas functions.</span></span> <span data-ttu-id="41cb3-137">Предполагается, что текстура будет интерполяция через сетку билинеарли.</span><span class="sxs-lookup"><span data-stu-id="41cb3-137">The texture is assumed to be interpolated over the mesh bilinearly.</span></span>

## <a name="requirements"></a><span data-ttu-id="41cb3-138">Требования</span><span class="sxs-lookup"><span data-stu-id="41cb3-138">Requirements</span></span>



| <span data-ttu-id="41cb3-139">Требование</span><span class="sxs-lookup"><span data-stu-id="41cb3-139">Requirement</span></span> | <span data-ttu-id="41cb3-140">Значение</span><span class="sxs-lookup"><span data-stu-id="41cb3-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41cb3-141">Header</span><span class="sxs-lookup"><span data-stu-id="41cb3-141">Header</span></span><br/>  | <dl> <span data-ttu-id="41cb3-142"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="41cb3-142"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="41cb3-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="41cb3-143">Library</span></span><br/> | <dl> <span data-ttu-id="41cb3-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41cb3-144"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41cb3-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41cb3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41cb3-146">Функции Уватлас</span><span class="sxs-lookup"><span data-stu-id="41cb3-146">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="41cb3-147">Использование Уватлас (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="41cb3-147">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
