---
description: Вычисляет ИМТ для каждого треугольника на основе пользовательского сигнала, определяемого приложением, который зависит от поверхности сетки (обычно с более высокой частотой, чем данные вершин). Сигнал вычисляется с помощью определяемой пользователем функции обратного вызова.
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: Функция D3DXComputeIMTFromSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 979304a350c226a9406e62896bb84492d8046e74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713795"
---
# <a name="d3dxcomputeimtfromsignal-function"></a><span data-ttu-id="64cca-104">Функция D3DXComputeIMTFromSignal</span><span class="sxs-lookup"><span data-stu-id="64cca-104">D3DXComputeIMTFromSignal function</span></span>

<span data-ttu-id="64cca-105">Вычисляет ИМТ для каждого треугольника на основе пользовательского сигнала, определяемого приложением, который зависит от поверхности сетки (обычно с более высокой частотой, чем данные вершин).</span><span class="sxs-lookup"><span data-stu-id="64cca-105">Calculates per-triangle IMT's from a custom application-specified signal that varies over the surface of the mesh (generally at a higher frequency than vertex data).</span></span> <span data-ttu-id="64cca-106">Сигнал вычисляется с помощью определяемой пользователем функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="64cca-106">The signal is evaluated via a user-specified callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="64cca-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64cca-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromSignal(
  _In_  LPD3DXMESH              pMesh,
  _In_  DWORD                   dwTextureIndex,
  _In_  UINT                    uSignalDimension,
  _In_  FLOAT                   fMaxUVDistance,
  _In_  DWORD                   dwOptions,
  _In_  LPD3DXIMTSIGNALCALLBACK pSignalCallback,
  _In_  VOID                    *pUserData,
        LPD3DXUVATLASCB         pStatusCallback,
        LPVOID                  pUserContext,
  _Out_ LPD3DXBUFFER            *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="64cca-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="64cca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64cca-109">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64cca-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64cca-110">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="64cca-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="64cca-111">Указатель на входную сетку (см. [**ID3DXMesh**](id3dxmesh.md)), которая содержит объект Geometry для вычисления ИМТ.</span><span class="sxs-lookup"><span data-stu-id="64cca-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="64cca-112">*двтекстуреиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64cca-112">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64cca-113">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64cca-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64cca-114">Отсчитываемый от нуля индекс координаты текстуры, определяющий, какой набор координат текстуры использовать.</span><span class="sxs-lookup"><span data-stu-id="64cca-114">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="64cca-115">*усигналдименсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64cca-115">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64cca-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64cca-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64cca-117">Количество компонентов в каждой точке данных в сигнале.</span><span class="sxs-lookup"><span data-stu-id="64cca-117">The number of components in each data point in the signal.</span></span>

</dd> <dt>

<span data-ttu-id="64cca-118">*фмаксувдистанце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64cca-118">*fMaxUVDistance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64cca-119">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64cca-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64cca-120">Максимальное расстояние между вершинами; алгоритм продолжит подразделения до тех пор, пока расстояние между всеми вершинами не меньше Фмаксувдистанце.</span><span class="sxs-lookup"><span data-stu-id="64cca-120">The maximum distance between vertices; the algorithm continues subdividing until the distance between all vertices is less than or equal to fMaxUVDistance.</span></span>

</dd> <dt>

<span data-ttu-id="64cca-121">*двоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64cca-121">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64cca-122">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64cca-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64cca-123">Параметры переноса текстур.</span><span class="sxs-lookup"><span data-stu-id="64cca-123">Texture wrap options.</span></span> <span data-ttu-id="64cca-124">Это сочетание одного или нескольких [**флагов D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="64cca-124">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="64cca-125">*псигналкаллбакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64cca-125">*pSignalCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64cca-126">Тип: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**</span><span class="sxs-lookup"><span data-stu-id="64cca-126">Type: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**</span></span>

<span data-ttu-id="64cca-127">Указатель на предоставляемую пользователем функцию оценщика, которая будет использоваться для вычисления значения сигнала в произвольных координатах U, V.</span><span class="sxs-lookup"><span data-stu-id="64cca-127">A pointer to a user-provided evaluator function, which will be used to compute the signal value at arbitrary U,V coordinates.</span></span> <span data-ttu-id="64cca-128">Функция соответствует прототипу [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).</span><span class="sxs-lookup"><span data-stu-id="64cca-128">The function follows the prototype of [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).</span></span>

</dd> <dt>

<span data-ttu-id="64cca-129">*пусердата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64cca-129">*pUserData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64cca-130">Тип: **void \***</span><span class="sxs-lookup"><span data-stu-id="64cca-130">Type: **VOID\***</span></span>

<span data-ttu-id="64cca-131">Указатель на определяемое пользователем значение, которое передается функции обратного вызова сигнала.</span><span class="sxs-lookup"><span data-stu-id="64cca-131">A pointer to a user-defined value which is passed to the signal callback function.</span></span> <span data-ttu-id="64cca-132">Обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="64cca-132">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="64cca-133">*пстатускаллбакк*</span><span class="sxs-lookup"><span data-stu-id="64cca-133">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="64cca-134">Тип: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="64cca-134">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="64cca-135">Указатель на функцию обратного вызова, чтобы отслеживать ход выполнения вычисления ИМТ.</span><span class="sxs-lookup"><span data-stu-id="64cca-135">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="64cca-136">*пусерконтекст*</span><span class="sxs-lookup"><span data-stu-id="64cca-136">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="64cca-137">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64cca-137">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64cca-138">Указатель на определяемую пользователем переменную, которая передается функции обратного вызова состояния.</span><span class="sxs-lookup"><span data-stu-id="64cca-138">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="64cca-139">Обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="64cca-139">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="64cca-140">*ппимтдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="64cca-140">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64cca-141">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="64cca-141">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="64cca-142">Указатель на буфер (см. [**ID3DXBuffer**](id3dxbuffer.md)), содержащий возвращенный массив ИМТ.</span><span class="sxs-lookup"><span data-stu-id="64cca-142">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="64cca-143">Этот массив может быть предоставлен в качестве входных данных для [функций D3DX уватлас](dx9-graphics-reference-d3dx-functions-uvatlas.md) , чтобы определить приоритет распределения пространства текстуры в параметризации текстуры.</span><span class="sxs-lookup"><span data-stu-id="64cca-143">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64cca-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64cca-144">Return value</span></span>

<span data-ttu-id="64cca-145">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64cca-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64cca-146">Если функция выполнена успешно, возвращается значение D3D \_ ОК. в противном случае — значение D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="64cca-146">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="64cca-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64cca-147">Remarks</span></span>

<span data-ttu-id="64cca-148">Эта функция требует, чтобы сетка входных данных содержала сопоставление текстур с сигналом-сеткой (в координатах текстуры).</span><span class="sxs-lookup"><span data-stu-id="64cca-148">This function requires that the input mesh contain a signal-to-mesh texture mapping (ie. texture coordinates).</span></span> <span data-ttu-id="64cca-149">Он позволяет пользователю произвольно определять сигнал на поверхности сети.</span><span class="sxs-lookup"><span data-stu-id="64cca-149">It allows the user to define a signal arbitrarily over the surface of the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="64cca-150">Требования</span><span class="sxs-lookup"><span data-stu-id="64cca-150">Requirements</span></span>



| <span data-ttu-id="64cca-151">Требование</span><span class="sxs-lookup"><span data-stu-id="64cca-151">Requirement</span></span> | <span data-ttu-id="64cca-152">Значение</span><span class="sxs-lookup"><span data-stu-id="64cca-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64cca-153">Header</span><span class="sxs-lookup"><span data-stu-id="64cca-153">Header</span></span><br/>  | <dl> <span data-ttu-id="64cca-154"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="64cca-154"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="64cca-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="64cca-155">Library</span></span><br/> | <dl> <span data-ttu-id="64cca-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64cca-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="64cca-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64cca-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64cca-158">Функции Уватлас</span><span class="sxs-lookup"><span data-stu-id="64cca-158">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="64cca-159">Использование Уватлас (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="64cca-159">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
