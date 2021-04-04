---
description: Тип объекта.
ms.assetid: ab405984-2ebc-4514-9400-bdb13676eda5
title: Перечисление D3DXPARAMETER_CLASS (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_CLASS
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: c42bfc9335c38de04ab484193a1e178a122f2210
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914700"
---
# <a name="d3dxparameter_class-enumeration"></a><span data-ttu-id="08843-103">\_Перечисление классов D3DXPARAMETER</span><span class="sxs-lookup"><span data-stu-id="08843-103">D3DXPARAMETER\_CLASS enumeration</span></span>

<span data-ttu-id="08843-104">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="08843-104">The type of object.</span></span>

## <a name="syntax"></a><span data-ttu-id="08843-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08843-105">Syntax</span></span>


```C++
typedef enum D3DXPARAMETER_CLASS { 
  D3DXPC_SCALAR,
  D3DXPC_VECTOR,
  D3DXPC_MATRIX_ROWS,
  D3DXPC_MATRIX_COLUMNS,
  D3DXPC_OBJECT,
  D3DXPC_STRUCT,
  D3DXPC_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_CLASS, *LPD3DXPARAMETER_CLASS;
```



## <a name="constants"></a><span data-ttu-id="08843-106">Константы</span><span class="sxs-lookup"><span data-stu-id="08843-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="08843-107"><span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**\_Скалярная D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="08843-107"><span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**D3DXPC\_SCALAR**</span></span>
</dt> <dd>

<span data-ttu-id="08843-108">Константа является скалярной.</span><span class="sxs-lookup"><span data-stu-id="08843-108">Constant is a scalar.</span></span>

</dd> <dt>

<span data-ttu-id="08843-109"><span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**\_Вектор D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="08843-109"><span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**D3DXPC\_VECTOR**</span></span>
</dt> <dd>

<span data-ttu-id="08843-110">Константа является вектором.</span><span class="sxs-lookup"><span data-stu-id="08843-110">Constant is a vector.</span></span>

</dd> <dt>

<span data-ttu-id="08843-111"><span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**D3DXPC \_ строк матрицы \_**</span><span class="sxs-lookup"><span data-stu-id="08843-111"><span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**D3DXPC\_MATRIX\_ROWS**</span></span>
</dt> <dd>

<span data-ttu-id="08843-112">Константа — это основная матрица строк.</span><span class="sxs-lookup"><span data-stu-id="08843-112">Constant is a row major matrix.</span></span>

</dd> <dt>

<span data-ttu-id="08843-113"><span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**\_Столбцы матрицы D3DXPC \_**</span><span class="sxs-lookup"><span data-stu-id="08843-113"><span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**D3DXPC\_MATRIX\_COLUMNS**</span></span>
</dt> <dd>

<span data-ttu-id="08843-114">Константа — это основная матрица столбца.</span><span class="sxs-lookup"><span data-stu-id="08843-114">Constant is a column major matrix.</span></span>

</dd> <dt>

<span data-ttu-id="08843-115"><span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**\_Объект D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="08843-115"><span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**D3DXPC\_OBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="08843-116">Константа — это либо текстура, либо шейдер, либо строка.</span><span class="sxs-lookup"><span data-stu-id="08843-116">Constant is either a texture, shader, or a string.</span></span>

</dd> <dt>

<span data-ttu-id="08843-117"><span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**\_Структура D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="08843-117"><span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**D3DXPC\_STRUCT**</span></span>
</dt> <dd>

<span data-ttu-id="08843-118">Константа является структурой.</span><span class="sxs-lookup"><span data-stu-id="08843-118">Constant is a structure.</span></span>

</dd> <dt>

<span data-ttu-id="08843-119"><span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="08843-119"><span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="08843-120">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="08843-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="08843-121">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="08843-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="08843-122">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="08843-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08843-123">Требования</span><span class="sxs-lookup"><span data-stu-id="08843-123">Requirements</span></span>



| <span data-ttu-id="08843-124">Требование</span><span class="sxs-lookup"><span data-stu-id="08843-124">Requirement</span></span> | <span data-ttu-id="08843-125">Значение</span><span class="sxs-lookup"><span data-stu-id="08843-125">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08843-126">Header</span><span class="sxs-lookup"><span data-stu-id="08843-126">Header</span></span><br/> | <dl> <span data-ttu-id="08843-127"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="08843-127"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08843-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08843-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08843-129">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="08843-129">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="08843-130">**D3DXSHADER \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="08843-130">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="08843-131">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="08843-131">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




