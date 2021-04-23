---
description: Вычисление нормалей единицы для каждой вершины в сетке. Предоставляется для поддержки устаревших приложений. Используйте D3DXComputeTangentFrameEx для улучшения результатов.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: Функция D3DXComputeNormals (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f95e5e353c318429f5340d1a831f9ca3050ba3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000414"
---
# <a name="d3dxcomputenormals-function"></a><span data-ttu-id="85f17-105">Функция D3DXComputeNormals</span><span class="sxs-lookup"><span data-stu-id="85f17-105">D3DXComputeNormals function</span></span>

<span data-ttu-id="85f17-106">Вычисление нормалей единицы для каждой вершины в сетке.</span><span class="sxs-lookup"><span data-stu-id="85f17-106">Computes unit normals for each vertex in a mesh.</span></span> <span data-ttu-id="85f17-107">Предоставляется для поддержки устаревших приложений.</span><span class="sxs-lookup"><span data-stu-id="85f17-107">Provided to support legacy applications.</span></span> <span data-ttu-id="85f17-108">Используйте [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) для улучшения результатов.</span><span class="sxs-lookup"><span data-stu-id="85f17-108">Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) for better results.</span></span>

## <a name="syntax"></a><span data-ttu-id="85f17-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85f17-109">Syntax</span></span>


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="85f17-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="85f17-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85f17-111">*пмеш* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="85f17-111">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85f17-112">Тип: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="85f17-112">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="85f17-113">Указатель на интерфейс [**ID3DXBaseMesh**](id3dxbasemesh.md) , представляющий Нормализованный объект сетки.</span><span class="sxs-lookup"><span data-stu-id="85f17-113">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the normalized mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="85f17-114">*паджаценци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85f17-114">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85f17-115">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="85f17-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="85f17-116">Указатель на массив из трех DWORD на грань, который указывает три соседа для каждого лица в созданной прогрессивной сетке.</span><span class="sxs-lookup"><span data-stu-id="85f17-116">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the created progressive mesh.</span></span> <span data-ttu-id="85f17-117">Этот параметр является необязательным и должен иметь значение **null** , если он не используется.</span><span class="sxs-lookup"><span data-stu-id="85f17-117">This parameter is optional and should be set to **NULL** if it is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85f17-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85f17-118">Return value</span></span>

<span data-ttu-id="85f17-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="85f17-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="85f17-120">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="85f17-120">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="85f17-121">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="85f17-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="85f17-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85f17-122">Remarks</span></span>

<span data-ttu-id="85f17-123">Входная сетка должна иметь флаг [D3DFVF " \_ стандартный](d3dfvf.md) ", заданный в его гибком формате вершин (фвф).</span><span class="sxs-lookup"><span data-stu-id="85f17-123">The input mesh must have the [D3DFVF\_NORMAL](d3dfvf.md) flag specified in its flexible vertex format (FVF).</span></span>

<span data-ttu-id="85f17-124">Нормальная вершина создается путем усреднения нормалей всех граней, совместно использующих эту вершину.</span><span class="sxs-lookup"><span data-stu-id="85f17-124">A normal for a vertex is generated by averaging the normals of all faces that share that vertex.</span></span>

<span data-ttu-id="85f17-125">Если задано соседство, реплицированные вершины игнорируются и «сглажены».</span><span class="sxs-lookup"><span data-stu-id="85f17-125">If adjacency is provided, replicated vertices are ignored and "smoothed" over.</span></span> <span data-ttu-id="85f17-126">Если значение соседа не задано, то реплицированные вершины будут иметь среднее значение среднего значения в только для лиц, явно ссылающихся на них.</span><span class="sxs-lookup"><span data-stu-id="85f17-126">If adjacency is not provided, replicated vertices will have normals averaged in from only the faces explicitly referencing them.</span></span>

<span data-ttu-id="85f17-127">Эта функция просто вызывает [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) со следующими входными параметрами:</span><span class="sxs-lookup"><span data-stu-id="85f17-127">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a><span data-ttu-id="85f17-128">Требования</span><span class="sxs-lookup"><span data-stu-id="85f17-128">Requirements</span></span>



| <span data-ttu-id="85f17-129">Требование</span><span class="sxs-lookup"><span data-stu-id="85f17-129">Requirement</span></span> | <span data-ttu-id="85f17-130">Значение</span><span class="sxs-lookup"><span data-stu-id="85f17-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85f17-131">Header</span><span class="sxs-lookup"><span data-stu-id="85f17-131">Header</span></span><br/>  | <dl> <span data-ttu-id="85f17-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="85f17-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="85f17-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85f17-133">Library</span></span><br/> | <dl> <span data-ttu-id="85f17-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85f17-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85f17-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85f17-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85f17-136">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="85f17-136">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
