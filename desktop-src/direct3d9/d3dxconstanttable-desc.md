---
description: Описание таблицы констант.
ms.assetid: 848b328a-95a4-4fd0-a7d4-4fb0e5d14f64
title: Структура D3DXCONSTANTTABLE_DESC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANTTABLE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7c53023952518182f68cf4a671ec47c6056a92a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821149"
---
# <a name="d3dxconstanttable_desc-structure"></a><span data-ttu-id="1fda3-103">\_Структура D3DXCONSTANTTABLE DESC</span><span class="sxs-lookup"><span data-stu-id="1fda3-103">D3DXCONSTANTTABLE\_DESC structure</span></span>

<span data-ttu-id="1fda3-104">Описание таблицы констант.</span><span class="sxs-lookup"><span data-stu-id="1fda3-104">A description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fda3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fda3-105">Syntax</span></span>


```C++
typedef struct D3DXCONSTANTTABLE_DESC {
  LPCSTR Creator;
  DWORD  Version;
  UINT   Constants;
} D3DXCONSTANTTABLE_DESC, *LPD3DXCONSTANTTABLE_DESC;
```



## <a name="members"></a><span data-ttu-id="1fda3-106">Члены</span><span class="sxs-lookup"><span data-stu-id="1fda3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1fda3-107">**Автор**</span><span class="sxs-lookup"><span data-stu-id="1fda3-107">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="1fda3-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fda3-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1fda3-109">Имя создателя таблицы констант.</span><span class="sxs-lookup"><span data-stu-id="1fda3-109">Name of the constant table creator.</span></span>

</dd> <dt>

<span data-ttu-id="1fda3-110">**Version**</span><span class="sxs-lookup"><span data-stu-id="1fda3-110">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="1fda3-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fda3-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1fda3-112">Версия шейдера.</span><span class="sxs-lookup"><span data-stu-id="1fda3-112">Shader version.</span></span>

</dd> <dt>

<span data-ttu-id="1fda3-113">**Константы**</span><span class="sxs-lookup"><span data-stu-id="1fda3-113">**Constants**</span></span>
</dt> <dd>

<span data-ttu-id="1fda3-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fda3-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1fda3-115">Число констант в таблице констант.</span><span class="sxs-lookup"><span data-stu-id="1fda3-115">Number of constants in the constant table.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1fda3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1fda3-116">Requirements</span></span>



| <span data-ttu-id="1fda3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1fda3-117">Requirement</span></span> | <span data-ttu-id="1fda3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1fda3-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fda3-119">Header</span><span class="sxs-lookup"><span data-stu-id="1fda3-119">Header</span></span><br/> | <dl> <span data-ttu-id="1fda3-120"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fda3-120"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fda3-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fda3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fda3-122">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="1fda3-122">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="1fda3-123">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="1fda3-123">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 
