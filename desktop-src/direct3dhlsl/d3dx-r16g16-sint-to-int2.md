---
title: Функция D3DX_R16G16_SINT_to_INT2
description: Распаковать \_ \_ \_ данные шейдера R16G16 Синт в формате DXGI в XMINT2.
ms.assetid: 0aad1581-5fd8-43c0-828d-51ef9eb82a74
keywords:
- Функция D3DX_R16G16_SINT_to_INT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SINT_to_INT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9e14e935b49e1fa0c982551696e8d38a076a5bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998654"
---
# <a name="d3dx_r16g16_sint_to_int2-function"></a><span data-ttu-id="8c912-104">D3DX \_ R16G16 \_ Синт \_ в \_ INT2 Function</span><span class="sxs-lookup"><span data-stu-id="8c912-104">D3DX\_R16G16\_SINT\_to\_INT2 function</span></span>

<span data-ttu-id="8c912-105">Распаковать \_ \_ \_ данные шейдера R16G16 Синт в формате DXGI в XMINT2.</span><span class="sxs-lookup"><span data-stu-id="8c912-105">Unpacks DXGI\_FORMAT\_R16G16\_SINT shader data to an XMINT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c912-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c912-106">Syntax</span></span>

``` syntax
XMINT2 D3DX_R16G16_SINT_to_INT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="8c912-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c912-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c912-108">*паккединпут*</span><span class="sxs-lookup"><span data-stu-id="8c912-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="8c912-109">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="8c912-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c912-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c912-110">Return value</span></span>

<span data-ttu-id="8c912-111">Распакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="8c912-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c912-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8c912-112">Requirements</span></span>



| <span data-ttu-id="8c912-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8c912-113">Requirement</span></span> | <span data-ttu-id="8c912-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8c912-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c912-115">Header</span><span class="sxs-lookup"><span data-stu-id="8c912-115">Header</span></span><br/> | <dl> <span data-ttu-id="8c912-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="8c912-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c912-117">См. также</span><span class="sxs-lookup"><span data-stu-id="8c912-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c912-118">Функции</span><span class="sxs-lookup"><span data-stu-id="8c912-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="8c912-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="8c912-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





