---
description: Вычисление ИМТ для каждого треугольника из данных на вершину. Эта функция позволяет вычислить ИМТ на основе любого значения в сетке (цвет, обычная и т. д.).
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: Функция D3DXComputeIMTFromPerVertexSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerVertexSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b12ea3f15f1a185125da46f575d37ad97dd5622
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713745"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a><span data-ttu-id="0a2b5-104">Функция D3DXComputeIMTFromPerVertexSignal</span><span class="sxs-lookup"><span data-stu-id="0a2b5-104">D3DXComputeIMTFromPerVertexSignal function</span></span>

<span data-ttu-id="0a2b5-105">Вычисление ИМТ для каждого треугольника из данных на вершину.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-105">Calculate per-triangle IMT's from from per-vertex data.</span></span> <span data-ttu-id="0a2b5-106">Эта функция позволяет вычислить ИМТ на основе любого значения в сетке (цвет, обычная и т. д.).</span><span class="sxs-lookup"><span data-stu-id="0a2b5-106">This function allows you to calculate the IMT based off of any value in a mesh (color, normal, etc).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a2b5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a2b5-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromPerVertexSignal(
  _In_        LPD3DXMESH      pMesh,
  _In_  const FLOAT           *pfVertexSignal,
  _In_        UINT            uSignalDimension,
  _In_        UINT            uSignalStride,
  _In_        DWORD           dwOptions,
              LPD3DXUVATLASCB pStatusCallback,
              LPVOID          pUserContext,
  _Out_       LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="0a2b5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a2b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a2b5-109">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0a2b5-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a2b5-110">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="0a2b5-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="0a2b5-111">Указатель на входную сетку (см. [**ID3DXMesh**](id3dxmesh.md)), которая содержит объект Geometry для вычисления ИМТ.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="0a2b5-112">*пфвертекссигнал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0a2b5-112">*pfVertexSignal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a2b5-113">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0a2b5-113">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0a2b5-114">Указатель на массив данных на вершину, из которого будут вычисляться ИМТ.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-114">A pointer to an array of per-vertex data from which IMT will be computed.</span></span> <span data-ttu-id="0a2b5-115">Размер массива — Усигналстриде \* v, где v — это количество вершин в сетке.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-115">The array size is uSignalStride \* v, where v is the number of vertices in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0a2b5-116">*усигналдименсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0a2b5-116">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a2b5-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a2b5-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a2b5-118">Количество плавающих элементов на вершину.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-118">The number of floats per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="0a2b5-119">*усигналстриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0a2b5-119">*uSignalStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a2b5-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a2b5-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a2b5-121">Число байтов на вершину в массиве.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-121">The number of bytes per vertex in the array.</span></span> <span data-ttu-id="0a2b5-122">Это должен быть кратный sizeof (float)</span><span class="sxs-lookup"><span data-stu-id="0a2b5-122">This must be a multiple of sizeof(float)</span></span>

</dd> <dt>

<span data-ttu-id="0a2b5-123">*двоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0a2b5-123">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a2b5-124">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a2b5-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a2b5-125">Параметры переноса текстур.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-125">Texture wrap options.</span></span> <span data-ttu-id="0a2b5-126">Это сочетание одного или нескольких [**флагов D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0a2b5-126">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a2b5-127">*пстатускаллбакк*</span><span class="sxs-lookup"><span data-stu-id="0a2b5-127">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="0a2b5-128">Тип: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="0a2b5-128">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="0a2b5-129">Указатель на функцию обратного вызова, чтобы отслеживать ход выполнения вычисления ИМТ.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-129">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="0a2b5-130">*пусерконтекст*</span><span class="sxs-lookup"><span data-stu-id="0a2b5-130">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="0a2b5-131">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a2b5-131">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a2b5-132">Указатель на определяемую пользователем переменную, которая передается функции обратного вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-132">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="0a2b5-133">Обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-133">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="0a2b5-134">*ппимтдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0a2b5-134">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a2b5-135">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a2b5-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0a2b5-136">Указатель на буфер (см. [**ID3DXBuffer**](id3dxbuffer.md)), содержащий возвращенный массив ИМТ.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-136">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="0a2b5-137">Этот массив может быть предоставлен в качестве входных данных для [функций D3DX уватлас](dx9-graphics-reference-d3dx-functions-uvatlas.md) , чтобы определить приоритет распределения пространства текстуры в параметризации текстуры.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-137">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a2b5-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a2b5-138">Return value</span></span>

<span data-ttu-id="0a2b5-139">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a2b5-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a2b5-140">Если функция выполнена успешно, возвращается значение D3D \_ ОК. в противном случае — значение D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="0a2b5-140">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a2b5-141">Требования</span><span class="sxs-lookup"><span data-stu-id="0a2b5-141">Requirements</span></span>



| <span data-ttu-id="0a2b5-142">Требование</span><span class="sxs-lookup"><span data-stu-id="0a2b5-142">Requirement</span></span> | <span data-ttu-id="0a2b5-143">Значение</span><span class="sxs-lookup"><span data-stu-id="0a2b5-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a2b5-144">Header</span><span class="sxs-lookup"><span data-stu-id="0a2b5-144">Header</span></span><br/>  | <dl> <span data-ttu-id="0a2b5-145"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a2b5-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0a2b5-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0a2b5-146">Library</span></span><br/> | <dl> <span data-ttu-id="0a2b5-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a2b5-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0a2b5-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a2b5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a2b5-149">Функции Уватлас</span><span class="sxs-lookup"><span data-stu-id="0a2b5-149">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="0a2b5-150">Использование Уватлас (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0a2b5-150">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
