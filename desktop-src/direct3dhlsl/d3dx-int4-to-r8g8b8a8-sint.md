---
title: Функция D3DX_INT4_to_R8G8B8A8_SINT
description: Упаковывает заданный XMINT4 обратно в формат DXGI \_ \_ R8G8B8A8 \_ Синт.
ms.assetid: ab9c5454-1673-43a9-ab76-bcd7b510b9a8
keywords:
- Функция D3DX_INT4_to_R8G8B8A8_SINT HLSL
topic_type:
- apiref
api_name:
- D3DX_INT4_to_R8G8B8A8_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9df4e4094ac96e7da2ccbff1da08e7aa1f7c4de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998336"
---
# <a name="d3dx_int4_to_r8g8b8a8_sint-function"></a><span data-ttu-id="06d26-104">D3DX \_ INT4 \_ to \_ R8G8B8A8 \_ Синт</span><span class="sxs-lookup"><span data-stu-id="06d26-104">D3DX\_INT4\_to\_R8G8B8A8\_SINT function</span></span>

<span data-ttu-id="06d26-105">Упаковывает заданный XMINT4 обратно в формат DXGI \_ \_ R8G8B8A8 \_ Синт.</span><span class="sxs-lookup"><span data-stu-id="06d26-105">Packs the given XMINT4 back into a DXGI\_FORMAT\_R8G8B8A8\_SINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="06d26-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06d26-106">Syntax</span></span>

``` syntax
UINT D3DX_INT4_to_R8G8B8A8_SINT(
   hlsl_precise XMINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="06d26-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="06d26-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06d26-108">*унпаккединпут*</span><span class="sxs-lookup"><span data-stu-id="06d26-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="06d26-109">Данные шейдера для упаковки.</span><span class="sxs-lookup"><span data-stu-id="06d26-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06d26-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06d26-110">Return value</span></span>

<span data-ttu-id="06d26-111">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="06d26-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="06d26-112">Требования</span><span class="sxs-lookup"><span data-stu-id="06d26-112">Requirements</span></span>



| <span data-ttu-id="06d26-113">Требование</span><span class="sxs-lookup"><span data-stu-id="06d26-113">Requirement</span></span> | <span data-ttu-id="06d26-114">Значение</span><span class="sxs-lookup"><span data-stu-id="06d26-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06d26-115">Header</span><span class="sxs-lookup"><span data-stu-id="06d26-115">Header</span></span><br/> | <dl> <span data-ttu-id="06d26-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="06d26-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06d26-117">См. также</span><span class="sxs-lookup"><span data-stu-id="06d26-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06d26-118">Функции</span><span class="sxs-lookup"><span data-stu-id="06d26-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="06d26-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="06d26-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





