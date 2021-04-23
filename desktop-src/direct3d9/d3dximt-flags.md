---
description: Параметры переноса текстур для API-интерфейсов вычисления ИМТ.
ms.assetid: ec364418-67c6-42c7-9c5d-b97aa7e17c24
title: Перечисление ФЛАГов D3DXIMT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 97731d4720e67fce899bf96f457e55f6adbc05a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694150"
---
# <a name="d3dximt-flags-enumeration"></a><span data-ttu-id="4a3a8-103">Перечисление ФЛАГов D3DXIMT</span><span class="sxs-lookup"><span data-stu-id="4a3a8-103">D3DXIMT FLAGS enumeration</span></span>

<span data-ttu-id="4a3a8-104">Параметры переноса текстур для API-интерфейсов вычисления ИМТ.</span><span class="sxs-lookup"><span data-stu-id="4a3a8-104">Texture wrapping options for IMT computation APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a3a8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a3a8-105">Syntax</span></span>


```C++
typedef enum D3DXIMT_FLAGS { 
  D3DXIMT_WRAP_U   = 1,
  D3DXIMT_WRAP_V   = 2,
  D3DXIMT_WRAP_UV  = 3
} D3DXIMT FLAGS, *LPD3DXIMT FLAGS;
```



## <a name="constants"></a><span data-ttu-id="4a3a8-106">Константы</span><span class="sxs-lookup"><span data-stu-id="4a3a8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4a3a8-107"><span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT в \_ оболочке \_ U**</span><span class="sxs-lookup"><span data-stu-id="4a3a8-107"><span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT\_WRAP\_U**</span></span>
</dt> <dd>

<span data-ttu-id="4a3a8-108">Текстура переносится в сторону U.</span><span class="sxs-lookup"><span data-stu-id="4a3a8-108">The texture wraps in the U direction.</span></span>

</dd> <dt>

<span data-ttu-id="4a3a8-109"><span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT \_ переносить \_ V**</span><span class="sxs-lookup"><span data-stu-id="4a3a8-109"><span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT\_WRAP\_V**</span></span>
</dt> <dd>

<span data-ttu-id="4a3a8-110">Текстура переносится в направлении V.</span><span class="sxs-lookup"><span data-stu-id="4a3a8-110">The texture wraps in the V direction.</span></span>

</dd> <dt>

<span data-ttu-id="4a3a8-111"><span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT \_ переносить \_ UV**</span><span class="sxs-lookup"><span data-stu-id="4a3a8-111"><span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT\_WRAP\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="4a3a8-112">Текстура переносится в обоих направлениях.</span><span class="sxs-lookup"><span data-stu-id="4a3a8-112">The texture wraps in both the U and V direction.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a3a8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="4a3a8-113">Requirements</span></span>



| <span data-ttu-id="4a3a8-114">Требование</span><span class="sxs-lookup"><span data-stu-id="4a3a8-114">Requirement</span></span> | <span data-ttu-id="4a3a8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4a3a8-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a3a8-116">Header</span><span class="sxs-lookup"><span data-stu-id="4a3a8-116">Header</span></span><br/> | <dl> <span data-ttu-id="4a3a8-117"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a3a8-117"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a3a8-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a3a8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a3a8-119">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="4a3a8-119">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="4a3a8-120">**D3DXComputeIMTFromSignal**</span><span class="sxs-lookup"><span data-stu-id="4a3a8-120">**D3DXComputeIMTFromSignal**</span></span>](d3dxcomputeimtfromsignal.md)
</dt> <dt>

[<span data-ttu-id="4a3a8-121">**D3DXComputeIMTFromTexture**</span><span class="sxs-lookup"><span data-stu-id="4a3a8-121">**D3DXComputeIMTFromTexture**</span></span>](d3dxcomputeimtfromtexture.md)
</dt> <dt>

[<span data-ttu-id="4a3a8-122">**D3DXComputeIMTFromPerTexelSignal**</span><span class="sxs-lookup"><span data-stu-id="4a3a8-122">**D3DXComputeIMTFromPerTexelSignal**</span></span>](d3dxcomputeimtfrompertexelsignal.md)
</dt> <dt>

[<span data-ttu-id="4a3a8-123">**D3DXComputeIMTFromPerVertexSignal**</span><span class="sxs-lookup"><span data-stu-id="4a3a8-123">**D3DXComputeIMTFromPerVertexSignal**</span></span>](d3dxcomputeimtfrompervertexsignal.md)
</dt> </dl>

 

 




