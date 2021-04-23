---
description: Описывает расположение включаемого файла.
ms.assetid: a15d363e-0d82-44a9-816b-edf2f60540b3
title: Перечисление D3DXINCLUDE_TYPE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINCLUDE_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 51a4ed41203a9f78ee5fef747f088e9def9033c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547887"
---
# <a name="d3dxinclude_type-enumeration"></a><span data-ttu-id="c4d26-103">\_Перечисление типов D3DXINCLUDE</span><span class="sxs-lookup"><span data-stu-id="c4d26-103">D3DXINCLUDE\_TYPE enumeration</span></span>

<span data-ttu-id="c4d26-104">Описывает расположение включаемого файла.</span><span class="sxs-lookup"><span data-stu-id="c4d26-104">Describes the location for the include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4d26-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4d26-105">Syntax</span></span>


```C++
typedef enum D3DXINCLUDE_TYPE { 
  D3DXINC_LOCAL        = 0,
  D3DXINC_SYSTEM       = 1,
  D3DXINC_FORCE_DWORD  = 0x7fffffff
} D3DXINCLUDE_TYPE, *LPD3DXINCLUDE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="c4d26-106">Константы</span><span class="sxs-lookup"><span data-stu-id="c4d26-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c4d26-107"><span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC \_ локальный**</span><span class="sxs-lookup"><span data-stu-id="c4d26-107"><span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC\_LOCAL**</span></span>
</dt> <dd>

<span data-ttu-id="c4d26-108">Найдите включаемый файл в локальном проекте.</span><span class="sxs-lookup"><span data-stu-id="c4d26-108">Look in the local project for the include file.</span></span>

</dd> <dt>

<span data-ttu-id="c4d26-109"><span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**D3DXINC \_ система**</span><span class="sxs-lookup"><span data-stu-id="c4d26-109"><span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**D3DXINC\_SYSTEM**</span></span>
</dt> <dd>

<span data-ttu-id="c4d26-110">Найдите в системном пути включаемого файла.</span><span class="sxs-lookup"><span data-stu-id="c4d26-110">Look in the system path for the include file.</span></span>

</dd> <dt>

<span data-ttu-id="c4d26-111"><span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c4d26-111"><span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c4d26-112">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="c4d26-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c4d26-113">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="c4d26-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c4d26-114">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="c4d26-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4d26-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c4d26-115">Requirements</span></span>



| <span data-ttu-id="c4d26-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c4d26-116">Requirement</span></span> | <span data-ttu-id="c4d26-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c4d26-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4d26-118">Header</span><span class="sxs-lookup"><span data-stu-id="c4d26-118">Header</span></span><br/> | <dl> <span data-ttu-id="c4d26-119"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4d26-119"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4d26-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4d26-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4d26-121">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="c4d26-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




