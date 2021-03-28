---
title: Структура D3DX11_GROUP_DESC (D3dx11effect. h)
description: Описывает группу эффектов.
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- D3DX11_GROUP_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_GROUP_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431daf0a14a465ee3533f1497278ddcd85b08a79
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081946"
---
# <a name="d3dx11_group_desc-structure"></a><span data-ttu-id="d64e8-104">\_ \_ Структура DESC группы D3DX11</span><span class="sxs-lookup"><span data-stu-id="d64e8-104">D3DX11\_GROUP\_DESC structure</span></span>

<span data-ttu-id="d64e8-105">Описывает группу эффектов.</span><span class="sxs-lookup"><span data-stu-id="d64e8-105">Describes an effect group.</span></span>

## <a name="syntax"></a><span data-ttu-id="d64e8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d64e8-106">Syntax</span></span>


```C++
typedef struct _D3DX11_GROUP_DESC {
  LPCSTR Name;
  UINT   Techniques;
  UINT   Annotations;
} D3DX11_GROUP_DESC;
```



## <a name="members"></a><span data-ttu-id="d64e8-107">Участники</span><span class="sxs-lookup"><span data-stu-id="d64e8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d64e8-108">**имя**;</span><span class="sxs-lookup"><span data-stu-id="d64e8-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="d64e8-109">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d64e8-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d64e8-110">Имя этой группы (только **значение NULL** , если глобальная).</span><span class="sxs-lookup"><span data-stu-id="d64e8-110">Name of this group (only **NULL** if global).</span></span>

</dd> <dt>

<span data-ttu-id="d64e8-111">**Технологий**</span><span class="sxs-lookup"><span data-stu-id="d64e8-111">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="d64e8-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d64e8-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d64e8-113">Количество методов, содержащихся в группе.</span><span class="sxs-lookup"><span data-stu-id="d64e8-113">Number of techniques contained in group.</span></span>

</dd> <dt>

<span data-ttu-id="d64e8-114">**Заметки**</span><span class="sxs-lookup"><span data-stu-id="d64e8-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="d64e8-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d64e8-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d64e8-116">Число заметок в этой группе.</span><span class="sxs-lookup"><span data-stu-id="d64e8-116">Number of annotations on this group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d64e8-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="d64e8-117">Remarks</span></span>

<span data-ttu-id="d64e8-118">D3DX11 \_ Group \_ DESC используется с [**ID3DX11EffectTechnique:: DESC**](id3dx11effecttechnique-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="d64e8-118">D3DX11\_GROUP\_DESC is used with [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d64e8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d64e8-119">Requirements</span></span>



| <span data-ttu-id="d64e8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d64e8-120">Requirement</span></span> | <span data-ttu-id="d64e8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d64e8-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d64e8-122">Header</span><span class="sxs-lookup"><span data-stu-id="d64e8-122">Header</span></span><br/> | <dl> <span data-ttu-id="d64e8-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d64e8-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d64e8-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d64e8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d64e8-125">Эффекты с 11 по структурам</span><span class="sxs-lookup"><span data-stu-id="d64e8-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

