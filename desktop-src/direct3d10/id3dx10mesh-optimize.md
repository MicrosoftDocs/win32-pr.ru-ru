---
description: Создает новую сетку с переупорядоченными лицами и вершинами для оптимизации производительности рисования.
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: 'Метод ID3DX10Mesh:: optimize (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e3c416b28cefe1a3f7fb487567afac4c99057478
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355273"
---
# <a name="id3dx10meshoptimize-method"></a><span data-ttu-id="eec6b-103">Метод ID3DX10Mesh:: OPTIMIZE</span><span class="sxs-lookup"><span data-stu-id="eec6b-103">ID3DX10Mesh::Optimize method</span></span>

<span data-ttu-id="eec6b-104">Создает новую сетку с переупорядоченными лицами и вершинами для оптимизации производительности рисования.</span><span class="sxs-lookup"><span data-stu-id="eec6b-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec6b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eec6b-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="eec6b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eec6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec6b-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eec6b-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec6b-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eec6b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eec6b-109">Указывает тип выполняемой оптимизации.</span><span class="sxs-lookup"><span data-stu-id="eec6b-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="eec6b-110">Этому параметру можно присвоить сочетание из одного или нескольких флагов из D3DXMESHOPT и D3DXMESH (за исключением D3DXMESH \_ 32-разрядной версии, D3DXMESH с помощью \_ \_ WriteOnly и D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="eec6b-110">This parameter can be set to a combination of one or more flags from D3DXMESHOPT and D3DXMESH (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="eec6b-111">*пфацеремап* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eec6b-111">*pFaceRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eec6b-112">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="eec6b-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="eec6b-113">Массив UINT, по одному на каждое лицо, определяющий исходную сетку, которая соответствует каждой грани в оптимизированной сетке.</span><span class="sxs-lookup"><span data-stu-id="eec6b-113">An array of UINTs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="eec6b-114">Если значение, заданное для этого аргумента, равно **null**, данные сопоставления лиц не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="eec6b-114">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="eec6b-115">*ппвертексремап* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="eec6b-115">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eec6b-116">Тип: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="eec6b-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="eec6b-117">Адрес указателя на [**интерфейс ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), который содержит DWORD для каждой вершины, указывающий, как новые вершины сопоставляются со старыми вершинами.</span><span class="sxs-lookup"><span data-stu-id="eec6b-117">Address of a pointer to an [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="eec6b-118">Такое перераспределение полезно, если необходимо изменить внешние данные на основе нового сопоставления вершин.</span><span class="sxs-lookup"><span data-stu-id="eec6b-118">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eec6b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eec6b-119">Return value</span></span>

<span data-ttu-id="eec6b-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eec6b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eec6b-121">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="eec6b-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eec6b-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eec6b-122">Remarks</span></span>

<span data-ttu-id="eec6b-123">Этот метод создает новую сетку.</span><span class="sxs-lookup"><span data-stu-id="eec6b-123">This method generates a new mesh.</span></span> <span data-ttu-id="eec6b-124">Перед запуском optimize приложение должно создать буфер соседей путем вызова [**ID3DX10Mesh:: женератеаджаценциандпоинтрепс**](id3dx10mesh-generateadjacencyandpointreps.md).</span><span class="sxs-lookup"><span data-stu-id="eec6b-124">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DX10Mesh::GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span></span> <span data-ttu-id="eec6b-125">В буфере соседка содержатся смежные данные, например список краев и сторон, расположенных рядом друг с другом.</span><span class="sxs-lookup"><span data-stu-id="eec6b-125">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="eec6b-126">Этот метод очень похож на метод [**ID3DX10Mesh:: клонемеш**](id3dx10mesh-clonemesh.md) , за исключением того, что он может выполнять оптимизацию при формировании нового клона сетки.</span><span class="sxs-lookup"><span data-stu-id="eec6b-126">This method is very similar to the [**ID3DX10Mesh::CloneMesh**](id3dx10mesh-clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="eec6b-127">Выходная сетка наследует все параметры создания входной сетки.</span><span class="sxs-lookup"><span data-stu-id="eec6b-127">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="eec6b-128">Требования</span><span class="sxs-lookup"><span data-stu-id="eec6b-128">Requirements</span></span>



| <span data-ttu-id="eec6b-129">Требование</span><span class="sxs-lookup"><span data-stu-id="eec6b-129">Requirement</span></span> | <span data-ttu-id="eec6b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="eec6b-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eec6b-131">Header</span><span class="sxs-lookup"><span data-stu-id="eec6b-131">Header</span></span><br/>  | <dl> <span data-ttu-id="eec6b-132"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="eec6b-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="eec6b-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eec6b-133">Library</span></span><br/> | <dl> <span data-ttu-id="eec6b-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eec6b-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eec6b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eec6b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec6b-136">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="eec6b-136">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="eec6b-137">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="eec6b-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
