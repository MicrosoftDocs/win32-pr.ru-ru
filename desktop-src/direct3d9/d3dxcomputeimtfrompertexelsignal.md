---
description: Вычислите ИМТ для каждого треугольника из данных шаг текселя. Эта функция похожа на D3DXComputeIMTFromTexture, но использует массив float для передачи данных и может вычислять более высокие значения измерений, чем 4.
ms.assetid: 4a151184-e67e-41e9-83c6-63da72f262fa
title: Функция D3DXComputeIMTFromPerTexelSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerTexelSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3db71fbc931f7bdb3e73c8d949a163607e66c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720899"
---
# <a name="d3dxcomputeimtfrompertexelsignal-function"></a><span data-ttu-id="273ef-104">Функция D3DXComputeIMTFromPerTexelSignal</span><span class="sxs-lookup"><span data-stu-id="273ef-104">D3DXComputeIMTFromPerTexelSignal function</span></span>

<span data-ttu-id="273ef-105">Вычислите ИМТ для каждого треугольника из данных шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="273ef-105">Calculate per-triangle IMT's from per-texel data.</span></span> <span data-ttu-id="273ef-106">Эта функция похожа на [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), но использует массив float для передачи данных и может вычислять более высокие значения измерений, чем 4.</span><span class="sxs-lookup"><span data-stu-id="273ef-106">This function is similar to [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), but it uses a float array to pass in the data, and it can calculate higher dimensional values than 4.</span></span>

## <a name="syntax"></a><span data-ttu-id="273ef-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="273ef-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromPerTexelSignal(
  _In_  LPD3DXMESH      pMesh,
  _In_  DWORD           dwTextureIndex,
  _In_  FLOAT           *pfTexelSignal,
  _In_  UINT            uWidth,
  _In_  UINT            uHeight,
  _In_  UINT            uSignalDimension,
  _In_  UINT            uComponents,
  _In_  DWORD           dwOptions,
        LPD3DXUVATLASCB pStatusCallback,
        LPVOID          pUserContext,
  _Out_ LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="273ef-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="273ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="273ef-109">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="273ef-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="273ef-110">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="273ef-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="273ef-111">Указатель на входную сетку (см. [**ID3DXMesh**](id3dxmesh.md)), которая содержит объект Geometry для вычисления ИМТ.</span><span class="sxs-lookup"><span data-stu-id="273ef-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="273ef-112">*двтекстуреиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="273ef-112">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="273ef-113">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="273ef-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="273ef-114">Отсчитываемый от нуля индекс координаты текстуры, определяющий, какой набор координат текстуры использовать.</span><span class="sxs-lookup"><span data-stu-id="273ef-114">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="273ef-115">*пфтекселсигнал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="273ef-115">*pfTexelSignal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="273ef-116">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="273ef-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="273ef-117">Указатель на массив входных пикселей текстуры, из которого будут вычисляться ИМТ.</span><span class="sxs-lookup"><span data-stu-id="273ef-117">A pointer to an array of input texels from which IMT will be computed.</span></span> <span data-ttu-id="273ef-118">Размер массива — Увидс \* ухеигхт \* укомпонентс.</span><span class="sxs-lookup"><span data-stu-id="273ef-118">The array size is uWidth\*uHeight\*uComponents.</span></span>

</dd> <dt>

<span data-ttu-id="273ef-119">*увидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="273ef-119">*uWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="273ef-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="273ef-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="273ef-121">Ширина текстуры в пикселях.</span><span class="sxs-lookup"><span data-stu-id="273ef-121">Texture width in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="273ef-122">*ухеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="273ef-122">*uHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="273ef-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="273ef-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="273ef-124">Высота текстуры в пикселях.</span><span class="sxs-lookup"><span data-stu-id="273ef-124">Texture height in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="273ef-125">*усигналдименсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="273ef-125">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="273ef-126">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="273ef-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="273ef-127">Количество плавающих элементов на компонент в каждом элементе массива сигналов.</span><span class="sxs-lookup"><span data-stu-id="273ef-127">The number of floats per-component in each element of the signal array.</span></span>

</dd> <dt>

<span data-ttu-id="273ef-128">*укомпонентс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="273ef-128">*uComponents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="273ef-129">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="273ef-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="273ef-130">Число компонентов в каждом шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="273ef-130">The number of components in each texel.</span></span>

</dd> <dt>

<span data-ttu-id="273ef-131">*двоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="273ef-131">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="273ef-132">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="273ef-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="273ef-133">Параметры переноса текстур.</span><span class="sxs-lookup"><span data-stu-id="273ef-133">Texture wrap options.</span></span> <span data-ttu-id="273ef-134">Это сочетание одного или нескольких [**флагов D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="273ef-134">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="273ef-135">*пстатускаллбакк*</span><span class="sxs-lookup"><span data-stu-id="273ef-135">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="273ef-136">Тип: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="273ef-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="273ef-137">Указатель на функцию обратного вызова, чтобы отслеживать ход выполнения вычисления ИМТ.</span><span class="sxs-lookup"><span data-stu-id="273ef-137">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="273ef-138">*пусерконтекст*</span><span class="sxs-lookup"><span data-stu-id="273ef-138">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="273ef-139">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="273ef-139">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="273ef-140">Указатель на определяемую пользователем переменную, которая передается функции обратного вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="273ef-140">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="273ef-141">Обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="273ef-141">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="273ef-142">*ппимтдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="273ef-142">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="273ef-143">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="273ef-143">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="273ef-144">Указатель на буфер (см. [**ID3DXBuffer**](id3dxbuffer.md)), содержащий возвращенный массив ИМТ.</span><span class="sxs-lookup"><span data-stu-id="273ef-144">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="273ef-145">Этот массив может быть предоставлен в качестве входных данных для [функций D3DX уватлас](dx9-graphics-reference-d3dx-functions-uvatlas.md) , чтобы определить приоритет распределения пространства текстуры в параметризации текстуры.</span><span class="sxs-lookup"><span data-stu-id="273ef-145">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="273ef-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="273ef-146">Return value</span></span>

<span data-ttu-id="273ef-147">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="273ef-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="273ef-148">Если функция выполнена успешно, возвращается значение D3D \_ ОК. в противном случае — значение D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="273ef-148">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="273ef-149">Требования</span><span class="sxs-lookup"><span data-stu-id="273ef-149">Requirements</span></span>



| <span data-ttu-id="273ef-150">Требование</span><span class="sxs-lookup"><span data-stu-id="273ef-150">Requirement</span></span> | <span data-ttu-id="273ef-151">Значение</span><span class="sxs-lookup"><span data-stu-id="273ef-151">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="273ef-152">Header</span><span class="sxs-lookup"><span data-stu-id="273ef-152">Header</span></span><br/>  | <dl> <span data-ttu-id="273ef-153"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="273ef-153"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="273ef-154">Библиотека</span><span class="sxs-lookup"><span data-stu-id="273ef-154">Library</span></span><br/> | <dl> <span data-ttu-id="273ef-155"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="273ef-155"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="273ef-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="273ef-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="273ef-157">Функции Уватлас</span><span class="sxs-lookup"><span data-stu-id="273ef-157">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="273ef-158">Использование Уватлас (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="273ef-158">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
