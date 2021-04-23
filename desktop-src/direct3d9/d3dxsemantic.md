---
description: Семантика сопоставляет параметр с регистрами вершин или шейдеров пикселей. Они также могут быть необязательными описательными строками, присоединенными к параметрам, не относящимся к регистру.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: Структура D3DXSEMANTIC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSEMANTIC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 08a30ac4d669beb5b93f2823219cb167d9e8d67f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424373"
---
# <a name="d3dxsemantic-structure"></a><span data-ttu-id="aae43-104">Структура D3DXSEMANTIC</span><span class="sxs-lookup"><span data-stu-id="aae43-104">D3DXSEMANTIC structure</span></span>

<span data-ttu-id="aae43-105">Семантика сопоставляет параметр с регистрами вершин или шейдеров пикселей.</span><span class="sxs-lookup"><span data-stu-id="aae43-105">Semantics map a parameter to vertex or pixel shader registers.</span></span> <span data-ttu-id="aae43-106">Они также могут быть необязательными описательными строками, присоединенными к параметрам, не относящимся к регистру.</span><span class="sxs-lookup"><span data-stu-id="aae43-106">They can also be optional descriptive strings attached to non-register parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="aae43-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aae43-107">Syntax</span></span>


```C++
typedef struct D3DXSEMANTIC {
  UINT Usage;
  UINT UsageIndex;
} D3DXSEMANTIC, *LPD3DXSEMANTIC;
```



## <a name="members"></a><span data-ttu-id="aae43-108">Члены</span><span class="sxs-lookup"><span data-stu-id="aae43-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="aae43-109">**Использование**</span><span class="sxs-lookup"><span data-stu-id="aae43-109">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="aae43-110">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aae43-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aae43-111">Параметры, определяющие, как используются ресурсы.</span><span class="sxs-lookup"><span data-stu-id="aae43-111">Options that identify how resources are used.</span></span> <span data-ttu-id="aae43-112">См. [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="aae43-112">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="aae43-113">**усажеиндекс**</span><span class="sxs-lookup"><span data-stu-id="aae43-113">**UsageIndex**</span></span>
</dt> <dd>

<span data-ttu-id="aae43-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aae43-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="aae43-115">Параметры, изменяющие способ интерпретации использования.</span><span class="sxs-lookup"><span data-stu-id="aae43-115">Options that modify how the usage is interpreted.</span></span> <span data-ttu-id="aae43-116">Индекс использования и использования составляют объявление вершины.</span><span class="sxs-lookup"><span data-stu-id="aae43-116">The usage and usage index make up a vertex declaration.</span></span> <span data-ttu-id="aae43-117">См. [Описание вершины (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="aae43-117">See [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aae43-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aae43-118">Remarks</span></span>

<span data-ttu-id="aae43-119">Семантика необходима для построителя вершин и пиксельного шейдера, входных и выходных регистров.</span><span class="sxs-lookup"><span data-stu-id="aae43-119">Semantics are required for vertex and pixel shader, input and output registers.</span></span>

## <a name="requirements"></a><span data-ttu-id="aae43-120">Требования</span><span class="sxs-lookup"><span data-stu-id="aae43-120">Requirements</span></span>



| <span data-ttu-id="aae43-121">Требование</span><span class="sxs-lookup"><span data-stu-id="aae43-121">Requirement</span></span> | <span data-ttu-id="aae43-122">Значение</span><span class="sxs-lookup"><span data-stu-id="aae43-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aae43-123">Header</span><span class="sxs-lookup"><span data-stu-id="aae43-123">Header</span></span><br/> | <dl> <span data-ttu-id="aae43-124"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="aae43-124"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aae43-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aae43-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae43-126">Структуры эффектов</span><span class="sxs-lookup"><span data-stu-id="aae43-126">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
