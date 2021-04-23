---
description: Описывает функцию, используемую в результате действия.
ms.assetid: 5d9deb82-7fe5-4408-8a6a-b34ecd97e8ba
title: Структура D3DXFUNCTION_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFUNCTION_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: ec53cae4689ebc1795937012259b2e219630568b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694152"
---
# <a name="d3dxfunction_desc-structure"></a><span data-ttu-id="48f1b-103">\_Структура D3DXFUNCTION DESC</span><span class="sxs-lookup"><span data-stu-id="48f1b-103">D3DXFUNCTION\_DESC structure</span></span>

<span data-ttu-id="48f1b-104">Описывает функцию, используемую в результате действия.</span><span class="sxs-lookup"><span data-stu-id="48f1b-104">Describes a function used by an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="48f1b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48f1b-105">Syntax</span></span>


```C++
typedef struct D3DXFUNCTION_DESC {
  LPCSTR Name;
  UINT   Annotations;
} D3DXFUNCTION_DESC, *LPD3DXFUNCTION_DESC;
```



## <a name="members"></a><span data-ttu-id="48f1b-106">Члены</span><span class="sxs-lookup"><span data-stu-id="48f1b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="48f1b-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="48f1b-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="48f1b-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48f1b-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="48f1b-109">Имя функции.</span><span class="sxs-lookup"><span data-stu-id="48f1b-109">Function name.</span></span>

</dd> <dt>

<span data-ttu-id="48f1b-110">**Заметки**</span><span class="sxs-lookup"><span data-stu-id="48f1b-110">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="48f1b-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48f1b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="48f1b-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="48f1b-112">Unused.</span></span> <span data-ttu-id="48f1b-113">Этому элементу всегда будет присвоено значение 0, [**жетфунктиондеск**](id3dxbaseeffect--getfunctiondesc.md).</span><span class="sxs-lookup"><span data-stu-id="48f1b-113">This member will always be set to zero by [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48f1b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="48f1b-114">Requirements</span></span>



| <span data-ttu-id="48f1b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="48f1b-115">Requirement</span></span> | <span data-ttu-id="48f1b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="48f1b-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f1b-117">Header</span><span class="sxs-lookup"><span data-stu-id="48f1b-117">Header</span></span><br/> | <dl> <span data-ttu-id="48f1b-118"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="48f1b-118"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48f1b-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48f1b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f1b-120">Структуры эффектов</span><span class="sxs-lookup"><span data-stu-id="48f1b-120">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
