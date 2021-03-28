---
title: Функция D3DX_R16G16_FLOAT_to_FLOAT2
description: Распаковка формата DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB Data Shader в XMFLOAT2.
ms.assetid: 6c57dc86-d034-4b54-8572-44ac3738beb9
keywords:
- Функция D3DX_R16G16_FLOAT_to_FLOAT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_FLOAT_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fb721e59a63415f98216b6e3f81a92e7598f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157239"
---
# <a name="d3dx_r16g16_float_to_float2-function"></a><span data-ttu-id="7de25-104">D3DX \_ R16G16 \_ с плавающей запятой \_ в \_ FLOAT2 функцию</span><span class="sxs-lookup"><span data-stu-id="7de25-104">D3DX\_R16G16\_FLOAT\_to\_FLOAT2 function</span></span>

<span data-ttu-id="7de25-105">Распаковка формата DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB Data Shader в XMFLOAT2.</span><span class="sxs-lookup"><span data-stu-id="7de25-105">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="7de25-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7de25-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="7de25-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7de25-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7de25-108">*паккединпут*</span><span class="sxs-lookup"><span data-stu-id="7de25-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="7de25-109">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="7de25-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7de25-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7de25-110">Return value</span></span>

<span data-ttu-id="7de25-111">Распакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="7de25-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="7de25-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7de25-112">Requirements</span></span>



| <span data-ttu-id="7de25-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7de25-113">Requirement</span></span> | <span data-ttu-id="7de25-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7de25-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7de25-115">Header</span><span class="sxs-lookup"><span data-stu-id="7de25-115">Header</span></span><br/> | <dl> <span data-ttu-id="7de25-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="7de25-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7de25-117">См. также</span><span class="sxs-lookup"><span data-stu-id="7de25-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7de25-118">Функции</span><span class="sxs-lookup"><span data-stu-id="7de25-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="7de25-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="7de25-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





