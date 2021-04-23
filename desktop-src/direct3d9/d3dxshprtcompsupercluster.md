---
description: Используется с сжатыми результатами симулятора предварительно вычисленной радианценой пересылки (PRT).
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: Функция D3DXSHPRTCompSuperCluster (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSuperCluster
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1daf25dddfaf738ecc2fed9605429a19170177ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354710"
---
# <a name="d3dxshprtcompsupercluster-function"></a><span data-ttu-id="406a6-103">Функция D3DXSHPRTCompSuperCluster</span><span class="sxs-lookup"><span data-stu-id="406a6-103">D3DXSHPRTCompSuperCluster function</span></span>

<span data-ttu-id="406a6-104">Используется с сжатыми результатами симулятора предварительно вычисленной радианценой пересылки (PRT).</span><span class="sxs-lookup"><span data-stu-id="406a6-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="406a6-105">Создает "подкластеры", которые представляют собой группы кластеров, которые могут быть изображены в одном вызове Draw.</span><span class="sxs-lookup"><span data-stu-id="406a6-105">Generates "superclusters," which are groups of clusters that can be drawn in the same draw call.</span></span> <span data-ttu-id="406a6-106">Для группирования кластеров используется жадный алгоритм, который уменьшает перерисовки.</span><span class="sxs-lookup"><span data-stu-id="406a6-106">A greedy algorithm that minimizes overdraw is used to group the clusters.</span></span>

## <a name="syntax"></a><span data-ttu-id="406a6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="406a6-107">Syntax</span></span>


```C++
HRESULT D3DXSHPRTCompSuperCluster(
  _In_    UINT       *pClusterIDs,
  _In_    LPD3DXMESH pScene,
  _In_    UINT       MaxNumClusters,
  _In_    UINT       NumClusters,
  _Inout_ UINT       *pSClusterIDs,
  _Inout_ UINT       *pNumSCs
);
```



## <a name="parameters"></a><span data-ttu-id="406a6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="406a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="406a6-109">*пклустеридс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="406a6-109">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="406a6-110">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="406a6-110">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="406a6-111">Указатель на идентификаторы кластера Нумвертс (извлеченные из сжатого буфера).</span><span class="sxs-lookup"><span data-stu-id="406a6-111">Pointer to a NumVerts cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="406a6-112">*псцене* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="406a6-112">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="406a6-113">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="406a6-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="406a6-114">Указатель на сетку, которая представляет составной сцену, передаваемой симулятору.</span><span class="sxs-lookup"><span data-stu-id="406a6-114">Pointer to a mesh that represents composite scene passed to the simulator.</span></span> <span data-ttu-id="406a6-115">См. [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="406a6-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="406a6-116">*Макснумклустерс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="406a6-116">*MaxNumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="406a6-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="406a6-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="406a6-118">Максимальное количество кластеров, выделенных на один супер кластер.</span><span class="sxs-lookup"><span data-stu-id="406a6-118">Maximum number of clusters allocated per super cluster.</span></span>

</dd> <dt>

<span data-ttu-id="406a6-119">*Нумклустерс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="406a6-119">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="406a6-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="406a6-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="406a6-121">Количество кластеров, вычисленных в симуляторе.</span><span class="sxs-lookup"><span data-stu-id="406a6-121">Number of clusters computed in the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="406a6-122">*псклустеридс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="406a6-122">*pSClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="406a6-123">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="406a6-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="406a6-124">Указатель на массив длины *нумклустерс*.</span><span class="sxs-lookup"><span data-stu-id="406a6-124">Pointer to an array of length *NumClusters*.</span></span> <span data-ttu-id="406a6-125">Содержит индекс супер кластера, которому был назначен соответствующий кластер.</span><span class="sxs-lookup"><span data-stu-id="406a6-125">Contains the index of the super cluster to which the corresponding cluster was assigned.</span></span>

</dd> <dt>

<span data-ttu-id="406a6-126">*пнумскс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="406a6-126">*pNumSCs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="406a6-127">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="406a6-127">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="406a6-128">Количество выделенных супер кластеров.</span><span class="sxs-lookup"><span data-stu-id="406a6-128">Number of super clusters allocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="406a6-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="406a6-129">Return value</span></span>

<span data-ttu-id="406a6-130">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="406a6-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="406a6-131">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="406a6-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="406a6-132">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="406a6-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="406a6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="406a6-133">Requirements</span></span>



| <span data-ttu-id="406a6-134">Требование</span><span class="sxs-lookup"><span data-stu-id="406a6-134">Requirement</span></span> | <span data-ttu-id="406a6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="406a6-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="406a6-136">Header</span><span class="sxs-lookup"><span data-stu-id="406a6-136">Header</span></span><br/>  | <dl> <span data-ttu-id="406a6-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="406a6-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="406a6-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="406a6-138">Library</span></span><br/> | <dl> <span data-ttu-id="406a6-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="406a6-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="406a6-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="406a6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="406a6-141">Предварительно вычисленные функции пересылки Радианце</span><span class="sxs-lookup"><span data-stu-id="406a6-141">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
