---
title: Структура D3DX11_EFFECT_VARIABLE_DESC (D3dx11effect. h)
description: Описывает переменную Effect.
ms.assetid: 9c975ad4-b90e-4e69-b78f-4f5cc61083ff
keywords:
- D3DX11_EFFECT_VARIABLE_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_VARIABLE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a83121c930c5a634434161c998c72215e227f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998693"
---
# <a name="d3dx11_effect_variable_desc-structure"></a><span data-ttu-id="d75df-104">\_ \_ Структура desc переменной влияния D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="d75df-104">D3DX11\_EFFECT\_VARIABLE\_DESC structure</span></span>

<span data-ttu-id="d75df-105">Описывает переменную Effect.</span><span class="sxs-lookup"><span data-stu-id="d75df-105">Describes an effect variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d75df-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d75df-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_VARIABLE_DESC {
  LPCSTR Name;
  LPCSTR Semantic;
  UINT   Flags;
  UINT   Annotations;
  UINT   BufferOffset;
  UINT   ExplicitBindPoint;
} D3DX11_EFFECT_VARIABLE_DESC;
```



## <a name="members"></a><span data-ttu-id="d75df-107">Участники</span><span class="sxs-lookup"><span data-stu-id="d75df-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d75df-108">**имя**;</span><span class="sxs-lookup"><span data-stu-id="d75df-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="d75df-109">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d75df-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d75df-110">Имя этой переменной, заметки или члена структуры.</span><span class="sxs-lookup"><span data-stu-id="d75df-110">Name of this variable, annotation, or structure member.</span></span>

</dd> <dt>

<span data-ttu-id="d75df-111">**Семантическ**</span><span class="sxs-lookup"><span data-stu-id="d75df-111">**Semantic**</span></span>
</dt> <dd>

<span data-ttu-id="d75df-112">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d75df-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d75df-113">Семантическая строка этой переменной или члена структуры (значение NULL для заметок или если отсутствует).</span><span class="sxs-lookup"><span data-stu-id="d75df-113">Semantic string of this variable or structure member (NULL for annotations or if not present).</span></span>

</dd> <dt>

<span data-ttu-id="d75df-114">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="d75df-114">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="d75df-115">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d75df-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d75df-116">Необязательные флаги для переменных эффектов.</span><span class="sxs-lookup"><span data-stu-id="d75df-116">Optional flags for effect variables.</span></span>

</dd> <dt>

<span data-ttu-id="d75df-117">**Заметки**</span><span class="sxs-lookup"><span data-stu-id="d75df-117">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="d75df-118">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d75df-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d75df-119">Число заметок для этой переменной (для заметок значение всегда равно 0).</span><span class="sxs-lookup"><span data-stu-id="d75df-119">Number of annotations on this variable (always 0 for annotations).</span></span>

</dd> <dt>

<span data-ttu-id="d75df-120">**буффероффсет**</span><span class="sxs-lookup"><span data-stu-id="d75df-120">**BufferOffset**</span></span>
</dt> <dd>

<span data-ttu-id="d75df-121">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d75df-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d75df-122">Смещение, содержащее кбуффер или тбуффер (всегда 0 для заметок или переменных, не содержащихся в буферах констант).</span><span class="sxs-lookup"><span data-stu-id="d75df-122">Offset into containing cbuffer or tbuffer (always 0 for annotations or variables not in constant buffers).</span></span>

</dd> <dt>

<span data-ttu-id="d75df-123">**експлиЦитбиндпоинт**</span><span class="sxs-lookup"><span data-stu-id="d75df-123">**ExplicitBindPoint**</span></span>
</dt> <dd>

<span data-ttu-id="d75df-124">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d75df-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="d75df-125">Используется, если переменная была явно привязана с помощью ключевого слова Register.</span><span class="sxs-lookup"><span data-stu-id="d75df-125">Used if the variable has been explicitly bound using the register keyword.</span></span> <span data-ttu-id="d75df-126">Проверьте флаги для \_ переменной влияния D3DX11 \_ \_ явной \_ \_ точки привязки.</span><span class="sxs-lookup"><span data-stu-id="d75df-126">Check Flags for D3DX11\_EFFECT\_VARIABLE\_EXPLICIT\_BIND\_POINT.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d75df-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="d75df-127">Remarks</span></span>

<span data-ttu-id="d75df-128">\_ПЕРЕМЕННАЯ D3DX11 \_ Effect \_ DESC используется с [**ID3DX11EffectVariable:: DESC**](id3dx11effectvariable-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="d75df-128">D3DX11\_EFFECT\_VARIABLE\_DESC is used with [**ID3DX11EffectVariable::GetDesc**](id3dx11effectvariable-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d75df-129">Требования</span><span class="sxs-lookup"><span data-stu-id="d75df-129">Requirements</span></span>



| <span data-ttu-id="d75df-130">Требование</span><span class="sxs-lookup"><span data-stu-id="d75df-130">Requirement</span></span> | <span data-ttu-id="d75df-131">Значение</span><span class="sxs-lookup"><span data-stu-id="d75df-131">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d75df-132">Header</span><span class="sxs-lookup"><span data-stu-id="d75df-132">Header</span></span><br/> | <dl> <span data-ttu-id="d75df-133"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d75df-133"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d75df-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d75df-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d75df-135">Эффекты с 11 по структурам</span><span class="sxs-lookup"><span data-stu-id="d75df-135">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

