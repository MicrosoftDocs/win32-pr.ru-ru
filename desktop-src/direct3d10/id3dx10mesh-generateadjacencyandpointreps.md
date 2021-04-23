---
description: Создание списка границ сетки, а также списка лиц, совместно использующих каждое ребро.
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: 'Метод ID3DX10Mesh:: Женератеаджаценциандпоинтрепс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateAdjacencyAndPointReps
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c46cf83931c95116132798ca971f9d4e61da2af8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548015"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a><span data-ttu-id="26f99-103">Метод ID3DX10Mesh:: Женератеаджаценциандпоинтрепс</span><span class="sxs-lookup"><span data-stu-id="26f99-103">ID3DX10Mesh::GenerateAdjacencyAndPointReps method</span></span>

<span data-ttu-id="26f99-104">Создание списка границ сетки, а также списка лиц, совместно использующих каждое ребро.</span><span class="sxs-lookup"><span data-stu-id="26f99-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f99-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26f99-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a><span data-ttu-id="26f99-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="26f99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f99-107">*Эпсилон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26f99-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26f99-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26f99-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26f99-109">Указывает, что вершины, отличающиеся от позиций меньше Эпсилон, должны рассматриваться как коинЦидент.</span><span class="sxs-lookup"><span data-stu-id="26f99-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f99-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26f99-110">Return value</span></span>

<span data-ttu-id="26f99-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26f99-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26f99-112">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="26f99-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26f99-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26f99-113">Remarks</span></span>

<span data-ttu-id="26f99-114">После того как приложение создаст сведения о смежности для сетки, данные сетки можно оптимизировать для повышения производительности рисования.</span><span class="sxs-lookup"><span data-stu-id="26f99-114">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="26f99-115">Порядок записей в смежном буфере определяется порядком индексов вершин в буфере индекса.</span><span class="sxs-lookup"><span data-stu-id="26f99-115">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="26f99-116">Смежный треугольник 0 всегда соответствует границе между индексами углов 0 и 1.</span><span class="sxs-lookup"><span data-stu-id="26f99-116">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="26f99-117">Смежный треугольник 1 всегда соответствует границе между индексами углов 1 и 2, а смежный треугольник 2 соответствует границе между индексами углов 2 и 0.</span><span class="sxs-lookup"><span data-stu-id="26f99-117">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="26f99-118">Требования</span><span class="sxs-lookup"><span data-stu-id="26f99-118">Requirements</span></span>



| <span data-ttu-id="26f99-119">Требование</span><span class="sxs-lookup"><span data-stu-id="26f99-119">Requirement</span></span> | <span data-ttu-id="26f99-120">Значение</span><span class="sxs-lookup"><span data-stu-id="26f99-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26f99-121">Header</span><span class="sxs-lookup"><span data-stu-id="26f99-121">Header</span></span><br/>  | <dl> <span data-ttu-id="26f99-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="26f99-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="26f99-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="26f99-123">Library</span></span><br/> | <dl> <span data-ttu-id="26f99-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26f99-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f99-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26f99-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f99-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="26f99-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="26f99-127">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="26f99-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
