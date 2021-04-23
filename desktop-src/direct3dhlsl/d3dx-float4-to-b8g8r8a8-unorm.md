---
title: Функция D3DX_FLOAT4_to_B8G8R8A8_UNORM
description: Упаковывает заданный XMFLOAT4 обратно в формат DXGI \_ \_ B8G8R8A8 \_ UNORM.
ms.assetid: 5b7452ed-446a-4760-83e6-f3209ac8daf4
keywords:
- Функция D3DX_FLOAT4_to_B8G8R8A8_UNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec0922218b9770d7a0c4cb4877f6144eded900
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986870"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm-function"></a><span data-ttu-id="6186f-104">D3DX \_ FLOAT4 \_ to \_ B8G8R8A8 \_ UNORM Function</span><span class="sxs-lookup"><span data-stu-id="6186f-104">D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM function</span></span>

<span data-ttu-id="6186f-105">Упаковывает заданный XMFLOAT4 обратно в формат DXGI \_ \_ B8G8R8A8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="6186f-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_B8G8R8A8\_UNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="6186f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6186f-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="6186f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6186f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6186f-108">*унпаккединпут*</span><span class="sxs-lookup"><span data-stu-id="6186f-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="6186f-109">Данные шейдера для упаковки.</span><span class="sxs-lookup"><span data-stu-id="6186f-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6186f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6186f-110">Return value</span></span>

<span data-ttu-id="6186f-111">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="6186f-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="6186f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="6186f-112">Requirements</span></span>



| <span data-ttu-id="6186f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="6186f-113">Requirement</span></span> | <span data-ttu-id="6186f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="6186f-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6186f-115">Header</span><span class="sxs-lookup"><span data-stu-id="6186f-115">Header</span></span><br/> | <dl> <span data-ttu-id="6186f-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="6186f-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6186f-117">См. также</span><span class="sxs-lookup"><span data-stu-id="6186f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6186f-118">Функции</span><span class="sxs-lookup"><span data-stu-id="6186f-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="6186f-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="6186f-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





