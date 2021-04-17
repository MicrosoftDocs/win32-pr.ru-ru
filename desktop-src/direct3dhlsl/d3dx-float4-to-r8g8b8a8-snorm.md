---
title: Функция D3DX_FLOAT4_to_R8G8B8A8_SNORM
description: Упаковывает заданный XMFLOAT4 обратно в формат DXGI \_ \_ R8G8B8A8 \_ снорм.
ms.assetid: 425aeabd-6249-4777-8935-827691abef24
keywords:
- Функция D3DX_FLOAT4_to_R8G8B8A8_SNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194835ef126a3441dc2b842784dfa841ae1d7d6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355780"
---
# <a name="d3dx_float4_to_r8g8b8a8_snorm-function"></a><span data-ttu-id="c86f2-104">D3DX \_ FLOAT4 \_ to \_ R8G8B8A8 \_ снорм Function</span><span class="sxs-lookup"><span data-stu-id="c86f2-104">D3DX\_FLOAT4\_to\_R8G8B8A8\_SNORM function</span></span>

<span data-ttu-id="c86f2-105">Упаковывает заданный XMFLOAT4 обратно в формат DXGI \_ \_ R8G8B8A8 \_ снорм.</span><span class="sxs-lookup"><span data-stu-id="c86f2-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R8G8B8A8\_SNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="c86f2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c86f2-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_SNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="c86f2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c86f2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c86f2-108">*унпаккединпут*</span><span class="sxs-lookup"><span data-stu-id="c86f2-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="c86f2-109">Данные шейдера для упаковки.</span><span class="sxs-lookup"><span data-stu-id="c86f2-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c86f2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c86f2-110">Return value</span></span>

<span data-ttu-id="c86f2-111">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="c86f2-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c86f2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="c86f2-112">Requirements</span></span>



| <span data-ttu-id="c86f2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="c86f2-113">Requirement</span></span> | <span data-ttu-id="c86f2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c86f2-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c86f2-115">Header</span><span class="sxs-lookup"><span data-stu-id="c86f2-115">Header</span></span><br/> | <dl> <span data-ttu-id="c86f2-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="c86f2-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c86f2-117">См. также</span><span class="sxs-lookup"><span data-stu-id="c86f2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c86f2-118">Функции</span><span class="sxs-lookup"><span data-stu-id="c86f2-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="c86f2-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="c86f2-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





