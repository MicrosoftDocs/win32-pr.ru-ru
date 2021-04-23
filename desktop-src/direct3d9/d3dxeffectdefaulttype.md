---
description: Типы данных эффектов. Данные содержатся в элементе pValue D3DXEFFECTDEFAULT.
ms.assetid: d698ad6e-2ce2-48d6-90be-49bc08f172a9
title: Перечисление D3DXEFFECTDEFAULTTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULTTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: ffd31167d712a8270011c061cd6328aa9214352e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694159"
---
# <a name="d3dxeffectdefaulttype-enumeration"></a><span data-ttu-id="52d12-104">Перечисление D3DXEFFECTDEFAULTTYPE</span><span class="sxs-lookup"><span data-stu-id="52d12-104">D3DXEFFECTDEFAULTTYPE enumeration</span></span>

<span data-ttu-id="52d12-105">Типы данных эффектов.</span><span class="sxs-lookup"><span data-stu-id="52d12-105">Effect data types.</span></span> <span data-ttu-id="52d12-106">Данные содержатся в элементе pValue [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span><span class="sxs-lookup"><span data-stu-id="52d12-106">The data is contained in the pValue member of [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="52d12-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52d12-107">Syntax</span></span>


```C++
typedef enum D3DXEFFECTDEFAULTTYPE { 
  D3DXEDT_STRING      = 1,
  D3DXEDT_FLOATS      = 2,
  D3DXEDT_DWORD       = 3,
  D3DXEDT_FORCEDWORD  = 0x7fffffff
} D3DXEFFECTDEFAULTTYPE, *LPD3DXEFFECTDEFAULTTYPE;
```



## <a name="constants"></a><span data-ttu-id="52d12-108">Константы</span><span class="sxs-lookup"><span data-stu-id="52d12-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="52d12-109"><span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**\_Строка D3DXEDT**</span><span class="sxs-lookup"><span data-stu-id="52d12-109"><span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**D3DXEDT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="52d12-110">Тип данных является текстовой строкой ASCII, завершающейся НУЛЕМ.</span><span class="sxs-lookup"><span data-stu-id="52d12-110">The data type is a NULL-terminated ASCII text string.</span></span>

</dd> <dt>

<span data-ttu-id="52d12-111"><span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT с \_ плавающей запятой**</span><span class="sxs-lookup"><span data-stu-id="52d12-111"><span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT\_FLOATS**</span></span>
</dt> <dd>

<span data-ttu-id="52d12-112">Тип данных является массивом типа float.</span><span class="sxs-lookup"><span data-stu-id="52d12-112">The data type is an array of type float.</span></span> <span data-ttu-id="52d12-113">Число типов float в массиве задается параметром Нумбитес в [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span><span class="sxs-lookup"><span data-stu-id="52d12-113">The number of float types in the array is specified by NumBytes in [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span></span>

</dd> <dt>

<span data-ttu-id="52d12-114"><span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="52d12-114"><span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="52d12-115">Тип данных — DWORD.</span><span class="sxs-lookup"><span data-stu-id="52d12-115">The data type is a DWORD.</span></span>

</dd> <dt>

<span data-ttu-id="52d12-116"><span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT \_ форцедворд**</span><span class="sxs-lookup"><span data-stu-id="52d12-116"><span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT\_FORCEDWORD**</span></span>
</dt> <dd>

<span data-ttu-id="52d12-117">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="52d12-117">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="52d12-118">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="52d12-118">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="52d12-119">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="52d12-119">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52d12-120">Требования</span><span class="sxs-lookup"><span data-stu-id="52d12-120">Requirements</span></span>



| <span data-ttu-id="52d12-121">Требование</span><span class="sxs-lookup"><span data-stu-id="52d12-121">Requirement</span></span> | <span data-ttu-id="52d12-122">Значение</span><span class="sxs-lookup"><span data-stu-id="52d12-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52d12-123">Header</span><span class="sxs-lookup"><span data-stu-id="52d12-123">Header</span></span><br/> | <dl> <span data-ttu-id="52d12-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="52d12-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52d12-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52d12-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d12-126">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="52d12-126">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




