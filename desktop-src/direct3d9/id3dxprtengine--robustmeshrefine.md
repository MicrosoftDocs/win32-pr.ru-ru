---
description: Делит лиц на сетку, обеспечивая консервативную адаптивную выборку, которая не будет устранять функции в сети.
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: 'Метод ID3DXPRTEngine:: Робустмешрефине (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.RobustMeshRefine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65d49fcec3072956365ce1ed8dc5d7a11ce6c826
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703954"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a><span data-ttu-id="001d6-103">Метод ID3DXPRTEngine:: Робустмешрефине</span><span class="sxs-lookup"><span data-stu-id="001d6-103">ID3DXPRTEngine::RobustMeshRefine method</span></span>

<span data-ttu-id="001d6-104">Делит лиц на сетку, обеспечивая консервативную адаптивную выборку, которая не будет устранять функции в сети.</span><span class="sxs-lookup"><span data-stu-id="001d6-104">Subdivides faces on a mesh, allowing for conservative adaptive sampling that will not eliminate features on the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="001d6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="001d6-105">Syntax</span></span>


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a><span data-ttu-id="001d6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="001d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="001d6-107">*Минеджеленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="001d6-107">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="001d6-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="001d6-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="001d6-109">Минимальная длина грани, которая будет создана при адаптивной выборки.</span><span class="sxs-lookup"><span data-stu-id="001d6-109">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="001d6-110">При нулевом значении будет заменено разумное значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="001d6-110">If zero, a reasonable default value will be substituted.</span></span>

</dd> <dt>

<span data-ttu-id="001d6-111">*Макссубдив* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="001d6-111">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="001d6-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="001d6-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="001d6-113">Максимальный уровень подраздела лица, который будет использоваться в адаптивной выборки.</span><span class="sxs-lookup"><span data-stu-id="001d6-113">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span> <span data-ttu-id="001d6-114">Если значение равно нулю, заменяется значением по умолчанию, равным 5.</span><span class="sxs-lookup"><span data-stu-id="001d6-114">If zero, a default value of 5 will be substituted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="001d6-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="001d6-115">Return value</span></span>

<span data-ttu-id="001d6-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="001d6-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="001d6-117">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="001d6-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="001d6-118">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="001d6-118">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="001d6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="001d6-119">Requirements</span></span>



| <span data-ttu-id="001d6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="001d6-120">Requirement</span></span> | <span data-ttu-id="001d6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="001d6-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="001d6-122">Header</span><span class="sxs-lookup"><span data-stu-id="001d6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="001d6-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="001d6-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="001d6-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="001d6-124">Library</span></span><br/> | <dl> <span data-ttu-id="001d6-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="001d6-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="001d6-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="001d6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="001d6-127">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="001d6-127">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="001d6-128">**ID3DXPRTEngine:: Компутебаунцеадаптиве**</span><span class="sxs-lookup"><span data-stu-id="001d6-128">**ID3DXPRTEngine::ComputeBounceAdaptive**</span></span>](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[<span data-ttu-id="001d6-129">**ID3DXPRTEngine:: Компутедиректлигхтингшадаптиве**</span><span class="sxs-lookup"><span data-stu-id="001d6-129">**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**</span></span>](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
