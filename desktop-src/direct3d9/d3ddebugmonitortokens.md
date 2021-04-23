---
description: Определяет маркеры монитора отладки.
ms.assetid: c0df4c9f-a232-45cf-b543-e95ee84a4a8d
title: Перечисление D3DDEBUGMONITORTOKENS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEBUGMONITORTOKENS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 82c3ecfa7d197e1ab912dbafe0d26fcb2281e605
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000326"
---
# <a name="d3ddebugmonitortokens-enumeration"></a><span data-ttu-id="73067-103">Перечисление D3DDEBUGMONITORTOKENS</span><span class="sxs-lookup"><span data-stu-id="73067-103">D3DDEBUGMONITORTOKENS enumeration</span></span>

<span data-ttu-id="73067-104">Определяет маркеры монитора отладки.</span><span class="sxs-lookup"><span data-stu-id="73067-104">Defines the debug monitor tokens.</span></span>

## <a name="syntax"></a><span data-ttu-id="73067-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73067-105">Syntax</span></span>


```C++
typedef enum D3DDEBUGMONITORTOKENS { 
  D3DDMT_ENABLE       = 0,
  D3DDMT_DISABLE      = 1,
  D3DDMT_FORCE_DWORD  = 0x7fffffff
} D3DDEBUGMONITORTOKENS, *LPD3DDEBUGMONITORTOKENS;
```



## <a name="constants"></a><span data-ttu-id="73067-106">Константы</span><span class="sxs-lookup"><span data-stu-id="73067-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="73067-107"><span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**\_Включить D3DDMT**</span><span class="sxs-lookup"><span data-stu-id="73067-107"><span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**D3DDMT\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73067-108">Включите монитор отладки.</span><span class="sxs-lookup"><span data-stu-id="73067-108">Enable the debug monitor.</span></span>

</dd> <dt>

<span data-ttu-id="73067-109"><span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**\_Отключение D3DDMT**</span><span class="sxs-lookup"><span data-stu-id="73067-109"><span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**D3DDMT\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="73067-110">Отключите монитор отладки.</span><span class="sxs-lookup"><span data-stu-id="73067-110">Disable the debug monitor.</span></span>

</dd> <dt>

<span data-ttu-id="73067-111"><span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="73067-111"><span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="73067-112">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="73067-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="73067-113">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="73067-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="73067-114">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="73067-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73067-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73067-115">Remarks</span></span>

<span data-ttu-id="73067-116">Значения в этом перечислимом типе используются в \_ состоянии рендеринга D3DRS дебугмонитортокен и относятся только к отладочным сборкам.</span><span class="sxs-lookup"><span data-stu-id="73067-116">The values in this enumerated type are used by the D3DRS\_DEBUGMONITORTOKEN render state and are only relevant for debug builds.</span></span>

## <a name="requirements"></a><span data-ttu-id="73067-117">Требования</span><span class="sxs-lookup"><span data-stu-id="73067-117">Requirements</span></span>



| <span data-ttu-id="73067-118">Требование</span><span class="sxs-lookup"><span data-stu-id="73067-118">Requirement</span></span> | <span data-ttu-id="73067-119">Значение</span><span class="sxs-lookup"><span data-stu-id="73067-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73067-120">Header</span><span class="sxs-lookup"><span data-stu-id="73067-120">Header</span></span><br/> | <dl> <span data-ttu-id="73067-121"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="73067-121"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73067-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73067-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73067-123">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="73067-123">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="73067-124">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="73067-124">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
