---
description: Возвращает количество вершин в сетке.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: 'Метод ID3DX10Mesh:: Жетвертекскаунт (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 189be6ff6872cfb85c2f336c29dedef2e435382e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703891"
---
# <a name="id3dx10meshgetvertexcount-method"></a><span data-ttu-id="ea8a3-103">Метод ID3DX10Mesh:: Жетвертекскаунт</span><span class="sxs-lookup"><span data-stu-id="ea8a3-103">ID3DX10Mesh::GetVertexCount method</span></span>

<span data-ttu-id="ea8a3-104">Возвращает количество вершин в сетке.</span><span class="sxs-lookup"><span data-stu-id="ea8a3-104">Get the number of vertices in the mesh.</span></span> <span data-ttu-id="ea8a3-105">Сетка может содержать несколько буферов вершин (т. е. один буфер вершин может содержать все данные о положении, другой может состоять из всех данных о координатах текстуры и т. д.), однако каждый буфер вершин будет содержать одинаковое число элементов.</span><span class="sxs-lookup"><span data-stu-id="ea8a3-105">A mesh may contain multiple vertex buffers (i.e. one vertex buffer may contain all position data, another may contains all texture coordinate data, etc.), however each vertex buffer will contain the same number of elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea8a3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea8a3-106">Syntax</span></span>


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a><span data-ttu-id="ea8a3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea8a3-107">Parameters</span></span>

<span data-ttu-id="ea8a3-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ea8a3-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea8a3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea8a3-109">Return value</span></span>

<span data-ttu-id="ea8a3-110">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea8a3-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea8a3-111">Число вершин в сетке.</span><span class="sxs-lookup"><span data-stu-id="ea8a3-111">The number of vertices in the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea8a3-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ea8a3-112">Requirements</span></span>



| <span data-ttu-id="ea8a3-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ea8a3-113">Requirement</span></span> | <span data-ttu-id="ea8a3-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ea8a3-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8a3-115">Header</span><span class="sxs-lookup"><span data-stu-id="ea8a3-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ea8a3-116"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea8a3-116"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea8a3-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ea8a3-117">Library</span></span><br/> | <dl> <span data-ttu-id="ea8a3-118"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea8a3-118"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea8a3-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea8a3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea8a3-120">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ea8a3-120">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ea8a3-121">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="ea8a3-121">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
