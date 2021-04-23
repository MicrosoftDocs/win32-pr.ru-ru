---
description: Возвращает число элементов в объявлении вершины.
ms.assetid: 3ce24e59-0ec3-4d53-8bc8-8a5a7cdf53b2
title: Функция D3DXGetDeclLength (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5576b4b86d5238d4942e09d605f695c66136799a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713677"
---
# <a name="d3dxgetdecllength-function"></a><span data-ttu-id="4fa8b-103">Функция D3DXGetDeclLength</span><span class="sxs-lookup"><span data-stu-id="4fa8b-103">D3DXGetDeclLength function</span></span>

<span data-ttu-id="4fa8b-104">Возвращает число элементов в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="4fa8b-104">Returns the number of elements in the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fa8b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fa8b-105">Syntax</span></span>


```C++
UINT D3DXGetDeclLength(
  _In_ const D3DVERTEXELEMENT9 *pDecl
);
```



## <a name="parameters"></a><span data-ttu-id="4fa8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fa8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fa8b-107">*пдекл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4fa8b-107">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fa8b-108">Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="4fa8b-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="4fa8b-109">Указатель на объявление вершины.</span><span class="sxs-lookup"><span data-stu-id="4fa8b-109">A pointer to the vertex declaration.</span></span> <span data-ttu-id="4fa8b-110">См. [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="4fa8b-110">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fa8b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fa8b-111">Return value</span></span>

<span data-ttu-id="4fa8b-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4fa8b-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4fa8b-113">Число элементов в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="4fa8b-113">The number of elements in the vertex declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fa8b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4fa8b-114">Requirements</span></span>



| <span data-ttu-id="4fa8b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4fa8b-115">Requirement</span></span> | <span data-ttu-id="4fa8b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4fa8b-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa8b-117">Header</span><span class="sxs-lookup"><span data-stu-id="4fa8b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4fa8b-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fa8b-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4fa8b-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4fa8b-119">Library</span></span><br/> | <dl> <span data-ttu-id="4fa8b-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fa8b-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4fa8b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fa8b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fa8b-122">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="4fa8b-122">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
