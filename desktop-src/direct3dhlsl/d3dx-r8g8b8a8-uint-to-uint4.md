---
title: Функция D3DX_R8G8B8A8_UINT_to_UINT4
description: Распаковать \_ \_ \_ данные шейдера R8G8B8A8 uint в формате DXGI в XMUINT4.
ms.assetid: fe25041f-db18-4555-a77a-e8d487143aa6
keywords:
- Функция D3DX_R8G8B8A8_UINT_to_UINT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UINT_to_UINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a371a36e797e1bff17aff457e11b140e4775894
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986885"
---
# <a name="d3dx_r8g8b8a8_uint_to_uint4-function"></a><span data-ttu-id="98205-104">D3DX \_ R8G8B8A8 \_ uint \_ в \_ UINT4 Function</span><span class="sxs-lookup"><span data-stu-id="98205-104">D3DX\_R8G8B8A8\_UINT\_to\_UINT4 function</span></span>

<span data-ttu-id="98205-105">Распаковать \_ \_ \_ данные шейдера R8G8B8A8 uint в формате DXGI в XMUINT4.</span><span class="sxs-lookup"><span data-stu-id="98205-105">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UINT shader data to an XMUINT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="98205-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98205-106">Syntax</span></span>

``` syntax
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="98205-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="98205-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98205-108">*паккединпут*</span><span class="sxs-lookup"><span data-stu-id="98205-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="98205-109">Упакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="98205-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98205-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98205-110">Return value</span></span>

<span data-ttu-id="98205-111">Распакованные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="98205-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="98205-112">Требования</span><span class="sxs-lookup"><span data-stu-id="98205-112">Requirements</span></span>



| <span data-ttu-id="98205-113">Требование</span><span class="sxs-lookup"><span data-stu-id="98205-113">Requirement</span></span> | <span data-ttu-id="98205-114">Значение</span><span class="sxs-lookup"><span data-stu-id="98205-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98205-115">Header</span><span class="sxs-lookup"><span data-stu-id="98205-115">Header</span></span><br/> | <dl> <span data-ttu-id="98205-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="98205-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98205-117">См. также</span><span class="sxs-lookup"><span data-stu-id="98205-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98205-118">Функции</span><span class="sxs-lookup"><span data-stu-id="98205-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="98205-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="98205-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





