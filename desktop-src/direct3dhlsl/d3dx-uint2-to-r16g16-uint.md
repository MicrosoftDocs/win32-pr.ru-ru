---
title: Функция D3DX_UINT2_to_R16G16_UINT
description: Упаковывает заданный XMUINT2 обратно в формат DXGI \_ \_ R16G16 \_ uint.
ms.assetid: 1f8aef92-7f34-4020-8a7e-6204922fc6d4
keywords:
- Функция D3DX_UINT2_to_R16G16_UINT HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT2_to_R16G16_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59a20b62fc5d8078152ed483ae49afceeeda4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998399"
---
# <a name="d3dx_uint2_to_r16g16_uint-function"></a><span data-ttu-id="3ab4b-104">D3DX \_ UINT2 \_ to \_ R16G16 \_ uint, функция</span><span class="sxs-lookup"><span data-stu-id="3ab4b-104">D3DX\_UINT2\_to\_R16G16\_UINT function</span></span>

<span data-ttu-id="3ab4b-105">Упаковывает заданный XMUINT2 обратно в формат DXGI \_ \_ R16G16 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-105">Packs the given XMUINT2 back into a DXGI\_FORMAT\_R16G16\_UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ab4b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ab4b-106">Syntax</span></span>

``` syntax
UINT D3DX_UINT2_to_R16G16_UINT(
   hlsl_precise XMUINT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="3ab4b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ab4b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ab4b-108">*унпаккединпут*</span><span class="sxs-lookup"><span data-stu-id="3ab4b-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="3ab4b-109">Данные шейдера для упаковки.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ab4b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ab4b-110">Return value</span></span>

<span data-ttu-id="3ab4b-111">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ab4b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="3ab4b-112">Requirements</span></span>



| <span data-ttu-id="3ab4b-113">Требование</span><span class="sxs-lookup"><span data-stu-id="3ab4b-113">Requirement</span></span> | <span data-ttu-id="3ab4b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3ab4b-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab4b-115">Header</span><span class="sxs-lookup"><span data-stu-id="3ab4b-115">Header</span></span><br/> | <dl> <span data-ttu-id="3ab4b-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="3ab4b-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ab4b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="3ab4b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ab4b-118">Функции</span><span class="sxs-lookup"><span data-stu-id="3ab4b-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="3ab4b-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="3ab4b-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





