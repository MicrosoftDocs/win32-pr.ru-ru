---
title: Функция D3DX_INT2_to_R16G16_SINT
description: Упаковывает заданный XMINT2 обратно в формат DXGI \_ \_ R16G16 \_ Синт.
ms.assetid: dc37e8a3-31d4-4af6-9bc3-9aa5062c066a
keywords:
- Функция D3DX_INT2_to_R16G16_SINT HLSL
topic_type:
- apiref
api_name:
- D3DX_INT2_to_R16G16_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97d60ba29b2451dea973b4ec0453f3a4df2ecdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987188"
---
# <a name="d3dx_int2_to_r16g16_sint-function"></a><span data-ttu-id="cfd82-104">D3DX \_ INT2 \_ to \_ R16G16 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="cfd82-104">D3DX\_INT2\_to\_R16G16\_SINT function</span></span>

<span data-ttu-id="cfd82-105">Упаковывает заданный XMINT2 обратно в формат DXGI \_ \_ R16G16 \_ Синт.</span><span class="sxs-lookup"><span data-stu-id="cfd82-105">Packs the given XMINT2 back into a DXGI\_FORMAT\_R16G16\_SINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfd82-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfd82-106">Syntax</span></span>

``` syntax
UINT D3DX_INT2_to_R16G16_SINT(
   hlsl_precise XMINT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="cfd82-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfd82-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfd82-108">*унпаккединпут*</span><span class="sxs-lookup"><span data-stu-id="cfd82-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="cfd82-109">Данные шейдера для упаковки.</span><span class="sxs-lookup"><span data-stu-id="cfd82-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfd82-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cfd82-110">Return value</span></span>

<span data-ttu-id="cfd82-111">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="cfd82-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfd82-112">Требования</span><span class="sxs-lookup"><span data-stu-id="cfd82-112">Requirements</span></span>



| <span data-ttu-id="cfd82-113">Требование</span><span class="sxs-lookup"><span data-stu-id="cfd82-113">Requirement</span></span> | <span data-ttu-id="cfd82-114">Значение</span><span class="sxs-lookup"><span data-stu-id="cfd82-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfd82-115">Header</span><span class="sxs-lookup"><span data-stu-id="cfd82-115">Header</span></span><br/> | <dl> <span data-ttu-id="cfd82-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="cfd82-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfd82-117">См. также</span><span class="sxs-lookup"><span data-stu-id="cfd82-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfd82-118">Функции</span><span class="sxs-lookup"><span data-stu-id="cfd82-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="cfd82-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="cfd82-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





