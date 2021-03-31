---
description: Описывает проход для объекта Effect.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: Структура D3DXPASS_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPASS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a147f737057a5b2cff6ea436d9d2e47920a67a4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354150"
---
# <a name="d3dxpass_desc-structure"></a><span data-ttu-id="459a1-103">\_Структура D3DXPASS DESC</span><span class="sxs-lookup"><span data-stu-id="459a1-103">D3DXPASS\_DESC structure</span></span>

<span data-ttu-id="459a1-104">Описывает проход для объекта Effect.</span><span class="sxs-lookup"><span data-stu-id="459a1-104">Describes a pass for an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="459a1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="459a1-105">Syntax</span></span>


```C++
typedef struct D3DXPASS_DESC {
  LPCSTR      Name;
  UINT        Annotations;
  const DWORD *pVertexShaderFunction;
  const DWORD *pPixelShaderFunction;
} D3DXPASS_DESC, *LPD3DXPASS_DESC;
```



## <a name="members"></a><span data-ttu-id="459a1-106">Члены</span><span class="sxs-lookup"><span data-stu-id="459a1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="459a1-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="459a1-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="459a1-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="459a1-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="459a1-109">Строковое значение, используемое для прохода.</span><span class="sxs-lookup"><span data-stu-id="459a1-109">String value used for the pass.</span></span>

</dd> <dt>

<span data-ttu-id="459a1-110">**Заметки**</span><span class="sxs-lookup"><span data-stu-id="459a1-110">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="459a1-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="459a1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="459a1-112">Заметки представляют собой определяемые пользователем данные, которые могут быть присоединены к любому методу, параметру Pass или.</span><span class="sxs-lookup"><span data-stu-id="459a1-112">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="459a1-113">См. раздел [Добавление сведений, чтобы параметры вступили в действие с \_ заметками](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="459a1-113">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>

</dd> <dt>

<span data-ttu-id="459a1-114">**пвертексшадерфунктион**</span><span class="sxs-lookup"><span data-stu-id="459a1-114">**pVertexShaderFunction**</span></span>
</dt> <dd>

<span data-ttu-id="459a1-115">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="459a1-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="459a1-116">Указатель на функцию шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="459a1-116">Pointer to the vertex shader function.</span></span> <span data-ttu-id="459a1-117">Если результат создается с D3DXFX, [который \_ не может быть \_ клонирован](d3dxfx.md), эта структура возвращает **пустой** указатель при вызове методом [**жетпассдеск**](id3dxbaseeffect--getpassdesc.md).</span><span class="sxs-lookup"><span data-stu-id="459a1-117">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this structure will return a **NULL** pointer when called by [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span></span>

</dd> <dt>

<span data-ttu-id="459a1-118">**ппикселшадерфунктион**</span><span class="sxs-lookup"><span data-stu-id="459a1-118">**pPixelShaderFunction**</span></span>
</dt> <dd>

<span data-ttu-id="459a1-119">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="459a1-119">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="459a1-120">Указатель на функцию шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="459a1-120">Pointer to the pixel shader function.</span></span> <span data-ttu-id="459a1-121">Если результат создается с D3DXFX, [который \_ не может быть \_ клонирован](d3dxfx.md), эта структура возвращает **пустой** указатель при вызове методом [**жетпассдеск**](id3dxbaseeffect--getpassdesc.md).</span><span class="sxs-lookup"><span data-stu-id="459a1-121">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this structure will return a **NULL** pointer when called by [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="459a1-122">Требования</span><span class="sxs-lookup"><span data-stu-id="459a1-122">Requirements</span></span>



| <span data-ttu-id="459a1-123">Требование</span><span class="sxs-lookup"><span data-stu-id="459a1-123">Requirement</span></span> | <span data-ttu-id="459a1-124">Значение</span><span class="sxs-lookup"><span data-stu-id="459a1-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="459a1-125">Header</span><span class="sxs-lookup"><span data-stu-id="459a1-125">Header</span></span><br/> | <dl> <span data-ttu-id="459a1-126"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="459a1-126"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="459a1-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="459a1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="459a1-128">Структуры эффектов</span><span class="sxs-lookup"><span data-stu-id="459a1-128">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[<span data-ttu-id="459a1-129">**жетпассдеск**</span><span class="sxs-lookup"><span data-stu-id="459a1-129">**GetPassDesc**</span></span>](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
