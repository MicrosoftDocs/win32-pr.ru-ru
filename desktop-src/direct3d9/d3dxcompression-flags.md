---
description: Определяет режим сжатия, используемый для хранения данных сжатого набора анимации.
ms.assetid: 41592b71-52ba-4727-a885-fb10fc23c5f8
title: Перечисление D3DXCOMPRESSION_FLAGS (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOMPRESSION_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 6f912c44659d418d543194ba82a9d82f31e7ef08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713746"
---
# <a name="d3dxcompression_flags-enumeration"></a><span data-ttu-id="dfebb-103">\_Перечисление флагов D3DXCOMPRESSION</span><span class="sxs-lookup"><span data-stu-id="dfebb-103">D3DXCOMPRESSION\_FLAGS enumeration</span></span>

<span data-ttu-id="dfebb-104">Определяет режим сжатия, используемый для хранения данных сжатого набора анимации.</span><span class="sxs-lookup"><span data-stu-id="dfebb-104">Defines the compression mode used for storing compressed animation set data.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfebb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfebb-105">Syntax</span></span>


```C++
typedef enum D3DXCOMPRESSION_FLAGS { 
  D3DXCOMPRESS_DEFAULT      = 0,
  D3DXCOMPRESS_STRONG       = 1,
  D3DXCOMPRESS_FORCE_DWORD  = 0x7fffffff
} D3DXCOMPRESSION_FLAGS, *LPD3DXCOMPRESSION_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="dfebb-106">Константы</span><span class="sxs-lookup"><span data-stu-id="dfebb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dfebb-107"><span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="dfebb-107"><span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="dfebb-108">Реализует быстрое сжатие.</span><span class="sxs-lookup"><span data-stu-id="dfebb-108">Implements fast compression.</span></span>

</dd> <dt>

<span data-ttu-id="dfebb-109"><span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS \_ strong**</span><span class="sxs-lookup"><span data-stu-id="dfebb-109"><span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS\_STRONG**</span></span>
</dt> <dd>

<span data-ttu-id="dfebb-110">Реализует низкую степень сжатия.</span><span class="sxs-lookup"><span data-stu-id="dfebb-110">Implements slow compression.</span></span> <span data-ttu-id="dfebb-111">Как правило, улучшается качество сжатой анимации, чем при \_ использовании D3DXCOMPRESS по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dfebb-111">Typically results in a better quality compressed animation set than if D3DXCOMPRESS\_DEFAULT is used.</span></span>

</dd> <dt>

<span data-ttu-id="dfebb-112"><span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="dfebb-112"><span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="dfebb-113">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="dfebb-113">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="dfebb-114">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="dfebb-114">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="dfebb-115">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="dfebb-115">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dfebb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dfebb-116">Requirements</span></span>



| <span data-ttu-id="dfebb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="dfebb-117">Requirement</span></span> | <span data-ttu-id="dfebb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dfebb-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfebb-119">Header</span><span class="sxs-lookup"><span data-stu-id="dfebb-119">Header</span></span><br/> | <dl> <span data-ttu-id="dfebb-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfebb-120"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfebb-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfebb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfebb-122">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="dfebb-122">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




