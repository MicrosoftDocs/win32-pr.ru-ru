---
title: Структура D3DX11_TECHNIQUE_DESC (D3dx11effect. h)
description: Описывает методику воздействия.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- D3DX11_TECHNIQUE_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TECHNIQUE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31158b93b8121ac3393e0935cee31c6361b894d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821261"
---
# <a name="d3dx11_technique_desc-structure"></a><span data-ttu-id="0f6a7-104">\_ \_ Структура DESC D3DX11 техника</span><span class="sxs-lookup"><span data-stu-id="0f6a7-104">D3DX11\_TECHNIQUE\_DESC structure</span></span>

<span data-ttu-id="0f6a7-105">Описывает методику воздействия.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-105">Describes an effect technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f6a7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f6a7-106">Syntax</span></span>


```C++
typedef struct _D3DX11_TECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DX11_TECHNIQUE_DESC;
```



## <a name="members"></a><span data-ttu-id="0f6a7-107">Участники</span><span class="sxs-lookup"><span data-stu-id="0f6a7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0f6a7-108">**имя**;</span><span class="sxs-lookup"><span data-stu-id="0f6a7-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="0f6a7-109">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0f6a7-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0f6a7-110">Имя этого метода (NULL, если он не является анонимным).</span><span class="sxs-lookup"><span data-stu-id="0f6a7-110">Name of this technique (NULL if not anonymous).</span></span>

</dd> <dt>

<span data-ttu-id="0f6a7-111">**Соответствующий**</span><span class="sxs-lookup"><span data-stu-id="0f6a7-111">**Passes**</span></span>
</dt> <dd>

<span data-ttu-id="0f6a7-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0f6a7-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0f6a7-113">Число проходов, содержащихся в методе.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-113">Number of passes contained in the technique.</span></span>

</dd> <dt>

<span data-ttu-id="0f6a7-114">**Заметки**</span><span class="sxs-lookup"><span data-stu-id="0f6a7-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="0f6a7-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0f6a7-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0f6a7-116">Число заметок на этом приеме.</span><span class="sxs-lookup"><span data-stu-id="0f6a7-116">Number of annotations on this technique.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f6a7-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="0f6a7-117">Remarks</span></span>

<span data-ttu-id="0f6a7-118">D3DX11 \_ техника \_ DESC используется с [**ID3DX11EffectTechnique:: DESC**](id3dx11effecttechnique-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="0f6a7-118">D3DX11\_TECHNIQUE\_DESC is used with [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f6a7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0f6a7-119">Requirements</span></span>



| <span data-ttu-id="0f6a7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0f6a7-120">Requirement</span></span> | <span data-ttu-id="0f6a7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0f6a7-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f6a7-122">Header</span><span class="sxs-lookup"><span data-stu-id="0f6a7-122">Header</span></span><br/> | <dl> <span data-ttu-id="0f6a7-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f6a7-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f6a7-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f6a7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f6a7-125">Эффекты с 11 по структурам</span><span class="sxs-lookup"><span data-stu-id="0f6a7-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

