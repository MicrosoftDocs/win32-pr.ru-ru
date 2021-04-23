---
title: Функция D3DX_R16G16_UINT_to_UINT2
description: Распаковать \_ \_ \_ данные шейдера R16G16 uint в формате DXGI в XMUINT2.
ms.assetid: bb24fdc4-db47-4cf3-af05-4b39c3af3701
keywords:
- Функция D3DX_R16G16_UINT_to_UINT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_UINT_to_UINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2586ff8876ee10368d49b816b38f5c9c8caf7c7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354043"
---
# <a name="d3dx_r16g16_uint_to_uint2-function"></a><span data-ttu-id="50e16-104">D3DX \_ R16G16 \_ uint \_ в \_ UINT2 Function</span><span class="sxs-lookup"><span data-stu-id="50e16-104">D3DX\_R16G16\_UINT\_to\_UINT2 function</span></span>

<span data-ttu-id="50e16-105">Распаковать \_ \_ \_ данные шейдера R16G16 uint в формате DXGI в XMUINT2.</span><span class="sxs-lookup"><span data-stu-id="50e16-105">Unpacks DXGI\_FORMAT\_R16G16\_UINT shader data to an XMUINT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e16-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50e16-106">Syntax</span></span>

``` syntax
XMUINT2 D3DX_R16G16_UINT_to_UINT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="50e16-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="50e16-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50e16-108">*паккединпут*</span><span class="sxs-lookup"><span data-stu-id="50e16-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="50e16-109">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="50e16-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50e16-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50e16-110">Return value</span></span>

<span data-ttu-id="50e16-111">Распакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="50e16-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="50e16-112">Требования</span><span class="sxs-lookup"><span data-stu-id="50e16-112">Requirements</span></span>



| <span data-ttu-id="50e16-113">Требование</span><span class="sxs-lookup"><span data-stu-id="50e16-113">Requirement</span></span> | <span data-ttu-id="50e16-114">Значение</span><span class="sxs-lookup"><span data-stu-id="50e16-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50e16-115">Header</span><span class="sxs-lookup"><span data-stu-id="50e16-115">Header</span></span><br/> | <dl> <span data-ttu-id="50e16-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="50e16-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50e16-117">См. также</span><span class="sxs-lookup"><span data-stu-id="50e16-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e16-118">Функции</span><span class="sxs-lookup"><span data-stu-id="50e16-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="50e16-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="50e16-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





