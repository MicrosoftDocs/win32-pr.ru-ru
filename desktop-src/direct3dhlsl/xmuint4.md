---
title: Структура XMUINT4
description: Описывает вектор целого числа без знака 4D.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- HLSL структура XMUINT4
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0b02ffe64e7b4c4479723b4e36abd87f6bd03b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986771"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="f5281-104">Структура XMUINT4</span><span class="sxs-lookup"><span data-stu-id="f5281-104">XMUINT4 structure</span></span>

<span data-ttu-id="f5281-105">Описывает вектор целого числа без знака 4D.</span><span class="sxs-lookup"><span data-stu-id="f5281-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5281-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5281-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a><span data-ttu-id="f5281-107">Участники</span><span class="sxs-lookup"><span data-stu-id="f5281-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f5281-108">**x**</span><span class="sxs-lookup"><span data-stu-id="f5281-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="f5281-109">компонент x вектора.</span><span class="sxs-lookup"><span data-stu-id="f5281-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="f5281-110">**y**</span><span class="sxs-lookup"><span data-stu-id="f5281-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="f5281-111">y-компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="f5281-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="f5281-112">**гармошкой**</span><span class="sxs-lookup"><span data-stu-id="f5281-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="f5281-113">z-компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="f5281-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="f5281-114">**w**</span><span class="sxs-lookup"><span data-stu-id="f5281-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="f5281-115">w — компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="f5281-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5281-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f5281-116">Requirements</span></span>



| <span data-ttu-id="f5281-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f5281-117">Requirement</span></span> | <span data-ttu-id="f5281-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f5281-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5281-119">Header</span><span class="sxs-lookup"><span data-stu-id="f5281-119">Header</span></span><br/> | <dl> <span data-ttu-id="f5281-120"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="f5281-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5281-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5281-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5281-122">Структуры</span><span class="sxs-lookup"><span data-stu-id="f5281-122">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="f5281-123">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="f5281-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





