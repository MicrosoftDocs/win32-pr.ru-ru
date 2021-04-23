---
title: Функция D3DX_R10G10B10A2_UINT_to_UINT4
description: Распаковать \_ \_ \_ данные шейдера R10G10B10A2 uint в формате DXGI в XMINT4.
ms.assetid: 47c4f11f-936a-46d5-9533-1a4f9fce6168
keywords:
- Функция D3DX_R10G10B10A2_UINT_to_UINT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R10G10B10A2_UINT_to_UINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378b013ad077c787253b4a58f24082d1c64b416f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987158"
---
# <a name="d3dx_r10g10b10a2_uint_to_uint4-function"></a><span data-ttu-id="ab85b-104">D3DX \_ R10G10B10A2 \_ uint \_ в \_ UINT4 Function</span><span class="sxs-lookup"><span data-stu-id="ab85b-104">D3DX\_R10G10B10A2\_UINT\_to\_UINT4 function</span></span>

<span data-ttu-id="ab85b-105">Распаковать \_ \_ \_ данные шейдера R10G10B10A2 uint в формате DXGI в XMINT4.</span><span class="sxs-lookup"><span data-stu-id="ab85b-105">Unpacks DXGI\_FORMAT\_R10G10B10A2\_UINT shader data to an XMINT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab85b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab85b-106">Syntax</span></span>

``` syntax
XMINT4 D3DX_R10G10B10A2_UINT_to_UINT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="ab85b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab85b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab85b-108">*паккединпут*</span><span class="sxs-lookup"><span data-stu-id="ab85b-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="ab85b-109">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="ab85b-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab85b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab85b-110">Return value</span></span>

<span data-ttu-id="ab85b-111">Распакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="ab85b-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab85b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ab85b-112">Requirements</span></span>



| <span data-ttu-id="ab85b-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ab85b-113">Requirement</span></span> | <span data-ttu-id="ab85b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ab85b-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab85b-115">Header</span><span class="sxs-lookup"><span data-stu-id="ab85b-115">Header</span></span><br/> | <dl> <span data-ttu-id="ab85b-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="ab85b-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab85b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="ab85b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab85b-118">Функции</span><span class="sxs-lookup"><span data-stu-id="ab85b-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="ab85b-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="ab85b-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





