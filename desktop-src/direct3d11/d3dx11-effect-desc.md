---
title: Структура D3DX11_EFFECT_DESC (D3dx11effect. h)
description: Описывает результат.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- D3DX11_EFFECT_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d43b37d13a8b3f076cc3c5967dac9a95ed18a5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987230"
---
# <a name="d3dx11_effect_desc-structure"></a><span data-ttu-id="7c4d2-104">\_Структура D3DX11 влияния на \_ структуру</span><span class="sxs-lookup"><span data-stu-id="7c4d2-104">D3DX11\_EFFECT\_DESC structure</span></span>

<span data-ttu-id="7c4d2-105">Описывает результат.</span><span class="sxs-lookup"><span data-stu-id="7c4d2-105">Describes an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c4d2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c4d2-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_DESC {
  UINT ConstantBuffers;
  UINT GlobalVariables;
  UINT InterfaceVariables;
  UINT Techniques;
  UINT Groups;
} D3DX11_EFFECT_DESC;
```



## <a name="members"></a><span data-ttu-id="7c4d2-107">Участники</span><span class="sxs-lookup"><span data-stu-id="7c4d2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c4d2-108">**константбуфферс**</span><span class="sxs-lookup"><span data-stu-id="7c4d2-108">**ConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="7c4d2-109">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c4d2-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7c4d2-110">Число буферов констант в этом результате.</span><span class="sxs-lookup"><span data-stu-id="7c4d2-110">Number of constant buffers in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="7c4d2-111">**глобалвариаблес**</span><span class="sxs-lookup"><span data-stu-id="7c4d2-111">**GlobalVariables**</span></span>
</dt> <dd>

<span data-ttu-id="7c4d2-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c4d2-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7c4d2-113">Число глобальных переменных в этом результате.</span><span class="sxs-lookup"><span data-stu-id="7c4d2-113">Number of global variables in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="7c4d2-114">**интерфацевариаблес**</span><span class="sxs-lookup"><span data-stu-id="7c4d2-114">**InterfaceVariables**</span></span>
</dt> <dd>

<span data-ttu-id="7c4d2-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c4d2-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7c4d2-116">Число глобальных интерфейсов в этом результате.</span><span class="sxs-lookup"><span data-stu-id="7c4d2-116">Number of global interfaces in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="7c4d2-117">**Технологий**</span><span class="sxs-lookup"><span data-stu-id="7c4d2-117">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="7c4d2-118">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c4d2-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7c4d2-119">Количество методов в этом результате.</span><span class="sxs-lookup"><span data-stu-id="7c4d2-119">Number of techniques in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="7c4d2-120">**Группы**</span><span class="sxs-lookup"><span data-stu-id="7c4d2-120">**Groups**</span></span>
</dt> <dd>

<span data-ttu-id="7c4d2-121">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7c4d2-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="7c4d2-122">Число групп в этом результате.</span><span class="sxs-lookup"><span data-stu-id="7c4d2-122">Number of groups in this effect.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c4d2-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="7c4d2-123">Remarks</span></span>

<span data-ttu-id="7c4d2-124">D3DX11 \_ Effect \_ DESC используется с [**ID3DX11Effect:: DESC**](id3dx11effect-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="7c4d2-124">D3DX11\_EFFECT\_DESC is used with [**ID3DX11Effect::GetDesc**](id3dx11effect-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c4d2-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7c4d2-125">Requirements</span></span>



| <span data-ttu-id="7c4d2-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7c4d2-126">Requirement</span></span> | <span data-ttu-id="7c4d2-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7c4d2-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4d2-128">Header</span><span class="sxs-lookup"><span data-stu-id="7c4d2-128">Header</span></span><br/> | <dl> <span data-ttu-id="7c4d2-129"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c4d2-129"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c4d2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c4d2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c4d2-131">Эффекты с 11 по структурам</span><span class="sxs-lookup"><span data-stu-id="7c4d2-131">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

