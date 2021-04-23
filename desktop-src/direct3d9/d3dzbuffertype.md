---
description: Определяет константы, описывающие форматы буферов глубины.
ms.assetid: 5e5ce48b-8859-43e0-a9b4-5972cf6bf781
title: Перечисление D3DZBUFFERTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DZBUFFERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 271a278f48c10a89fa6f552c3e1a7b4a83f274f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713741"
---
# <a name="d3dzbuffertype-enumeration"></a><span data-ttu-id="4a087-103">Перечисление D3DZBUFFERTYPE</span><span class="sxs-lookup"><span data-stu-id="4a087-103">D3DZBUFFERTYPE enumeration</span></span>

<span data-ttu-id="4a087-104">Определяет константы, описывающие форматы буферов глубины.</span><span class="sxs-lookup"><span data-stu-id="4a087-104">Defines constants that describe depth-buffer formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a087-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a087-105">Syntax</span></span>


```C++
typedef enum D3DZBUFFERTYPE { 
  D3DZB_FALSE        = 0,
  D3DZB_TRUE         = 1,
  D3DZB_USEW         = 2,
  D3DZB_FORCE_DWORD  = 0x7fffffff
} D3DZBUFFERTYPE, *LPD3DZBUFFERTYPE;
```



## <a name="constants"></a><span data-ttu-id="4a087-106">Константы</span><span class="sxs-lookup"><span data-stu-id="4a087-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4a087-107"><span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB \_ false**</span><span class="sxs-lookup"><span data-stu-id="4a087-107"><span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB\_FALSE**</span></span>
</dt> <dd>

<span data-ttu-id="4a087-108">Отключить буферизацию глубины.</span><span class="sxs-lookup"><span data-stu-id="4a087-108">Disable depth buffering.</span></span>

</dd> <dt>

<span data-ttu-id="4a087-109"><span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB \_ true**</span><span class="sxs-lookup"><span data-stu-id="4a087-109"><span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB\_TRUE**</span></span>
</dt> <dd>

<span data-ttu-id="4a087-110">Включить z-буферизацию.</span><span class="sxs-lookup"><span data-stu-id="4a087-110">Enable z-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="4a087-111"><span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB \_ усев**</span><span class="sxs-lookup"><span data-stu-id="4a087-111"><span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB\_USEW**</span></span>
</dt> <dd>

<span data-ttu-id="4a087-112">Включить w-Buffering.</span><span class="sxs-lookup"><span data-stu-id="4a087-112">Enable w-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="4a087-113"><span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4a087-113"><span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="4a087-114">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="4a087-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="4a087-115">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="4a087-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="4a087-116">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="4a087-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a087-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a087-117">Remarks</span></span>

<span data-ttu-id="4a087-118">Члены этого перечислимого типа используются с \_ состоянием отрисовки D3DRS зенабле.</span><span class="sxs-lookup"><span data-stu-id="4a087-118">Members of this enumerated type are used with the D3DRS\_ZENABLE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a087-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4a087-119">Requirements</span></span>



| <span data-ttu-id="4a087-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4a087-120">Requirement</span></span> | <span data-ttu-id="4a087-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4a087-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a087-122">Header</span><span class="sxs-lookup"><span data-stu-id="4a087-122">Header</span></span><br/> | <dl> <span data-ttu-id="4a087-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a087-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a087-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a087-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a087-125">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="4a087-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="4a087-126">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="4a087-126">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
