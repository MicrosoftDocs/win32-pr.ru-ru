---
description: '\_Структура КОНСТАНТИНФО D3DXSHADER'
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: Структура D3DXSHADER_CONSTANTINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: e90c0085035e78b9bc3ce1c48642157d8badc924
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273760"
---
# <a name="d3dxshader_constantinfo-structure"></a><span data-ttu-id="43b0c-103">\_Структура КОНСТАНТИНФО D3DXSHADER</span><span class="sxs-lookup"><span data-stu-id="43b0c-103">D3DXSHADER\_CONSTANTINFO structure</span></span>

## <a name="syntax"></a><span data-ttu-id="43b0c-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43b0c-104">Syntax</span></span>


```C++
typedef struct D3DXSHADER_CONSTANTINFO {
  DWORD Name;
  WORD  RegisterSet;
  WORD  RegisterIndex;
  WORD  RegisterCount;
  WORD  Reserved;
  DWORD TypeInfo;
  DWORD DefaultValue;
} D3DXSHADER_CONSTANTINFO, *LPD3DXSHADER_CONSTANTINFO;
```



## <a name="members"></a><span data-ttu-id="43b0c-105">Члены</span><span class="sxs-lookup"><span data-stu-id="43b0c-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="43b0c-106">**Name**</span><span class="sxs-lookup"><span data-stu-id="43b0c-106">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="43b0c-107">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43b0c-107">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43b0c-108">Смещение от начала этой структуры (в байтах) к строке, содержащей сведения о константе.</span><span class="sxs-lookup"><span data-stu-id="43b0c-108">Offset from the beginning of this structure, in bytes, to the string that contains the constant information.</span></span>

</dd> <dt>

<span data-ttu-id="43b0c-109">**Register**</span><span class="sxs-lookup"><span data-stu-id="43b0c-109">**RegisterSet**</span></span>
</dt> <dd>

<span data-ttu-id="43b0c-110">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43b0c-110">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43b0c-111">Набор регистров.</span><span class="sxs-lookup"><span data-stu-id="43b0c-111">Register set.</span></span> <span data-ttu-id="43b0c-112">См. раздел [**D3DXREGISTER \_ Set**](./d3dxregister-set.md).</span><span class="sxs-lookup"><span data-stu-id="43b0c-112">See [**D3DXREGISTER\_SET**](./d3dxregister-set.md).</span></span>

</dd> <dt>

<span data-ttu-id="43b0c-113">**регистериндекс**</span><span class="sxs-lookup"><span data-stu-id="43b0c-113">**RegisterIndex**</span></span>
</dt> <dd>

<span data-ttu-id="43b0c-114">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43b0c-114">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43b0c-115">Индекс регистра.</span><span class="sxs-lookup"><span data-stu-id="43b0c-115">The register index.</span></span>

</dd> <dt>

<span data-ttu-id="43b0c-116">**регистеркаунт**</span><span class="sxs-lookup"><span data-stu-id="43b0c-116">**RegisterCount**</span></span>
</dt> <dd>

<span data-ttu-id="43b0c-117">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43b0c-117">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43b0c-118">Количество регистров.</span><span class="sxs-lookup"><span data-stu-id="43b0c-118">Number of registers.</span></span>

</dd> <dt>

<span data-ttu-id="43b0c-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="43b0c-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="43b0c-120">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43b0c-120">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43b0c-121">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="43b0c-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="43b0c-122">**TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="43b0c-122">**TypeInfo**</span></span>
</dt> <dd>

<span data-ttu-id="43b0c-123">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43b0c-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43b0c-124">Смещение от начала этой структуры (в байтах) к строке, содержащей сведения о [**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="43b0c-124">Offset from the beginning of this structure, in bytes, to the string that contains the [**D3DXSHADER\_TYPEINFO**](d3dxshader-typeinfo.md) information.</span></span>

</dd> <dt>

<span data-ttu-id="43b0c-125">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="43b0c-125">**DefaultValue**</span></span>
</dt> <dd>

<span data-ttu-id="43b0c-126">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43b0c-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43b0c-127">Смещение от начала этой структуры (в байтах) к строке, содержащей значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="43b0c-127">Offset from the beginning of this structure, in bytes, to the string that contains the default value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="43b0c-128">Требования</span><span class="sxs-lookup"><span data-stu-id="43b0c-128">Requirements</span></span>



| <span data-ttu-id="43b0c-129">Требование</span><span class="sxs-lookup"><span data-stu-id="43b0c-129">Requirement</span></span> | <span data-ttu-id="43b0c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="43b0c-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43b0c-131">Header</span><span class="sxs-lookup"><span data-stu-id="43b0c-131">Header</span></span><br/> | <dl> <span data-ttu-id="43b0c-132"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="43b0c-132"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43b0c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43b0c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43b0c-134">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="43b0c-134">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
