---
description: Определяет тип режимов цикла набора анимации, используемых для воспроизведения.
ms.assetid: 2ce26bf0-2b33-4193-a58f-03493a051351
title: Перечисление D3DXPLAYBACK_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLAYBACK_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ce95b4765ec678c43c8e0ed92008deeb9927298
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914716"
---
# <a name="d3dxplayback_type-enumeration"></a><span data-ttu-id="3f9f9-103">\_Перечисление типов D3DXPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="3f9f9-103">D3DXPLAYBACK\_TYPE enumeration</span></span>

<span data-ttu-id="3f9f9-104">Определяет тип режимов цикла набора анимации, используемых для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3f9f9-104">Defines the type of animation set looping modes used for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f9f9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f9f9-105">Syntax</span></span>


```C++
typedef enum D3DXPLAYBACK_TYPE { 
  D3DXPLAY_LOOP         = 0,
  D3DXPLAY_ONCE         = 1,
  D3DXPLAY_PINGPONG     = 2,
  D3DXPLAY_FORCE_DWORD  = 0x7fffffff
} D3DXPLAYBACK_TYPE, *LPD3DXPLAYBACK_TYPE;
```



## <a name="constants"></a><span data-ttu-id="3f9f9-106">Константы</span><span class="sxs-lookup"><span data-stu-id="3f9f9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3f9f9-107"><span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**\_Цикл D3DXPLAY**</span><span class="sxs-lookup"><span data-stu-id="3f9f9-107"><span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**D3DXPLAY\_LOOP**</span></span>
</dt> <dd>

<span data-ttu-id="3f9f9-108">Анимация повторяется бесконечно.</span><span class="sxs-lookup"><span data-stu-id="3f9f9-108">The animation repeats endlessly.</span></span>

</dd> <dt>

<span data-ttu-id="3f9f9-109"><span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY \_ один раз**</span><span class="sxs-lookup"><span data-stu-id="3f9f9-109"><span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY\_ONCE**</span></span>
</dt> <dd>

<span data-ttu-id="3f9f9-110">Анимация воспроизводится один раз, а затем останавливается на последнем кадре.</span><span class="sxs-lookup"><span data-stu-id="3f9f9-110">The animation plays once, and then it stops on the last frame.</span></span>

</dd> <dt>

<span data-ttu-id="3f9f9-111"><span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY \_ пингпонг**</span><span class="sxs-lookup"><span data-stu-id="3f9f9-111"><span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY\_PINGPONG**</span></span>
</dt> <dd>

<span data-ttu-id="3f9f9-112">Анимация Дополнительно перемещается между воспроизведением вперед и воспроизведением назад.</span><span class="sxs-lookup"><span data-stu-id="3f9f9-112">The animation alternates endlessly between playing forward and playing backward.</span></span>

</dd> <dt>

<span data-ttu-id="3f9f9-113"><span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3f9f9-113"><span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="3f9f9-114">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="3f9f9-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="3f9f9-115">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="3f9f9-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="3f9f9-116">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="3f9f9-116">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f9f9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3f9f9-117">Requirements</span></span>



| <span data-ttu-id="3f9f9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3f9f9-118">Requirement</span></span> | <span data-ttu-id="3f9f9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3f9f9-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f9f9-120">Header</span><span class="sxs-lookup"><span data-stu-id="3f9f9-120">Header</span></span><br/> | <dl> <span data-ttu-id="3f9f9-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f9f9-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f9f9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f9f9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f9f9-123">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="3f9f9-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




