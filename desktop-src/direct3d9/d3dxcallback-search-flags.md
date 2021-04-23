---
description: Флаги, используемые для получения сведений о обратном вызове.
ms.assetid: e8126ff0-db23-4da6-a999-0efb8c2647da
title: Перечисление D3DXCALLBACK_SEARCH_FLAGS (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCALLBACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d3302b79734557a5c1f2082ec2a4e95c03790f4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081880"
---
# <a name="d3dxcallback_search_flags-enumeration"></a><span data-ttu-id="ac3de-103">\_ \_ Перечисление флагов поиска D3DXCALLBACK</span><span class="sxs-lookup"><span data-stu-id="ac3de-103">D3DXCALLBACK\_SEARCH\_FLAGS enumeration</span></span>

<span data-ttu-id="ac3de-104">Флаги, используемые для получения сведений о обратном вызове.</span><span class="sxs-lookup"><span data-stu-id="ac3de-104">Flags used to obtain callback information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac3de-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac3de-105">Syntax</span></span>


```C++
typedef enum D3DXCALLBACK_SEARCH_FLAGS { 
  D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION  = 1,
  D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION     = 2,
  D3DXCALLBACK_SEARCH_FORCE_DWORD                 = 0x7fffffff
} D3DXCALLBACK_SEARCH_FLAGS, *LPD3DXCALLBACK_SEARCH_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="ac3de-106">Константы</span><span class="sxs-lookup"><span data-stu-id="ac3de-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ac3de-107"><span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**Поиск D3DXCALLBACK, \_ \_ исключая \_ начальную \_ точку**</span><span class="sxs-lookup"><span data-stu-id="ac3de-107"><span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**D3DXCALLBACK\_SEARCH\_EXCLUDING\_INITIAL\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="ac3de-108">Исключить обратные вызовы, расположенные в начальной позиции из поиска.</span><span class="sxs-lookup"><span data-stu-id="ac3de-108">Exclude callbacks located at the initial position from the search.</span></span>

</dd> <dt>

<span data-ttu-id="ac3de-109"><span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**\_Поиск D3DXCALLBACK \_ за \_ начальной \_ позицией**</span><span class="sxs-lookup"><span data-stu-id="ac3de-109"><span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**D3DXCALLBACK\_SEARCH\_BEHIND\_INITIAL\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="ac3de-110">Измените направление поиска обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ac3de-110">Reverse the callback search direction.</span></span>

</dd> <dt>

<span data-ttu-id="ac3de-111"><span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK \_ Поиск \_ принудительный \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ac3de-111"><span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK\_SEARCH\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="ac3de-112">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="ac3de-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="ac3de-113">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="ac3de-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="ac3de-114">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="ac3de-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac3de-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ac3de-115">Requirements</span></span>



| <span data-ttu-id="ac3de-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ac3de-116">Requirement</span></span> | <span data-ttu-id="ac3de-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ac3de-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3de-118">Header</span><span class="sxs-lookup"><span data-stu-id="ac3de-118">Header</span></span><br/> | <dl> <span data-ttu-id="ac3de-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac3de-119"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac3de-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac3de-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac3de-121">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="ac3de-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




