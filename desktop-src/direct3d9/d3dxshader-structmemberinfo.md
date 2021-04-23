---
description: Вспомогательная структура, содержащая сведения о структуре элементов.
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: Структура D3DXSHADER_STRUCTMEMBERINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_STRUCTMEMBERINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 01782331459956c0878b46861db0d4f11e19c7dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354623"
---
# <a name="d3dxshader_structmemberinfo-structure"></a><span data-ttu-id="0879b-103">\_Структура СТРУКТМЕМБЕРИНФО D3DXSHADER</span><span class="sxs-lookup"><span data-stu-id="0879b-103">D3DXSHADER\_STRUCTMEMBERINFO structure</span></span>

<span data-ttu-id="0879b-104">Вспомогательная структура, содержащая сведения о структуре элементов.</span><span class="sxs-lookup"><span data-stu-id="0879b-104">A helper structure containing member structure information.</span></span>

## <a name="syntax"></a><span data-ttu-id="0879b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0879b-105">Syntax</span></span>


```C++
typedef struct D3DXSHADER_STRUCTMEMBERINFO {
  DWORD Name;
  DWORD TypeInfo;
} D3DXSHADER_STRUCTMEMBERINFO, *LPD3DXSHADER_STRUCTMEMBERINFO;
```



## <a name="members"></a><span data-ttu-id="0879b-106">Члены</span><span class="sxs-lookup"><span data-stu-id="0879b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0879b-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="0879b-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="0879b-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0879b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0879b-109">Смещение от начала этой структуры (в байтах) к строке, содержащей имя члена структуры.</span><span class="sxs-lookup"><span data-stu-id="0879b-109">Offset from the beginning of this structure, in bytes, to the string that contains the structure member name.</span></span>

</dd> <dt>

<span data-ttu-id="0879b-110">**TypeInfo**</span><span class="sxs-lookup"><span data-stu-id="0879b-110">**TypeInfo**</span></span>
</dt> <dd>

<span data-ttu-id="0879b-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0879b-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0879b-112">Смещение от начала этой структуры (в байтах) к строке, содержащей сведения о типе.</span><span class="sxs-lookup"><span data-stu-id="0879b-112">Offset from the beginning of this structure, in bytes, to the string that contains the type information.</span></span> <span data-ttu-id="0879b-113">См. [**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md).</span><span class="sxs-lookup"><span data-stu-id="0879b-113">See [**D3DXSHADER\_TYPEINFO**](d3dxshader-typeinfo.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0879b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0879b-114">Requirements</span></span>



| <span data-ttu-id="0879b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0879b-115">Requirement</span></span> | <span data-ttu-id="0879b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0879b-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0879b-117">Header</span><span class="sxs-lookup"><span data-stu-id="0879b-117">Header</span></span><br/> | <dl> <span data-ttu-id="0879b-118"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0879b-118"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0879b-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0879b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0879b-120">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="0879b-120">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="0879b-121">**D3DXSHADER \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="0879b-121">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
