---
title: Функция D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
description: Распаковка формата DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB Data Shader в XMFLOAT4. | Функция D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
ms.assetid: f709267f-8dcd-47c8-b4cf-3cc903a08c35
keywords:
- Функция D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c813c74569dbd23d17fbe93b6b34f3e39f86bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998303"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4_inexact-function"></a><span data-ttu-id="e9103-105">D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 \_ Точная функция</span><span class="sxs-lookup"><span data-stu-id="e9103-105">D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact function</span></span>

<span data-ttu-id="e9103-106">Распаковка формата DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB Data Shader в XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="e9103-106">Unpacks DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9103-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9103-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="e9103-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9103-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9103-109">*паккединпут*</span><span class="sxs-lookup"><span data-stu-id="e9103-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="e9103-110">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="e9103-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9103-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9103-111">Return value</span></span>

<span data-ttu-id="e9103-112">Распакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="e9103-112">The unpacked shader data.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9103-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="e9103-113">Remarks</span></span>

<span data-ttu-id="e9103-114">Эта функция использует инструкции шейдера, которые не имеют достаточно высокой точности для получения точного ответа.</span><span class="sxs-lookup"><span data-stu-id="e9103-114">This function uses shader instructions that don't have high enough precision to give the exact answer.</span></span> <span data-ttu-id="e9103-115">Альтернативная функция [**D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md) использует таблицу подстановки, хранящуюся в шейдере, чтобы дать точное преобразование sRGB для преобразования с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="e9103-115">The alternative function [**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md) uses a lookup table stored in the shader to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9103-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e9103-116">Requirements</span></span>



| <span data-ttu-id="e9103-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e9103-117">Requirement</span></span> | <span data-ttu-id="e9103-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e9103-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9103-119">Header</span><span class="sxs-lookup"><span data-stu-id="e9103-119">Header</span></span><br/> | <dl> <span data-ttu-id="e9103-120"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="e9103-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9103-121">См. также</span><span class="sxs-lookup"><span data-stu-id="e9103-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9103-122">Функции</span><span class="sxs-lookup"><span data-stu-id="e9103-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="e9103-123">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="e9103-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





