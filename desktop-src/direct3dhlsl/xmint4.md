---
title: Структура XMINT4
description: Описывает целочисленный вектор 4D.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- HLSL структура XMINT4
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302d820428fafb1561bd38850c4f75240ce9094f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355380"
---
# <a name="xmint4-structure"></a><span data-ttu-id="91416-104">Структура XMINT4</span><span class="sxs-lookup"><span data-stu-id="91416-104">XMINT4 structure</span></span>

<span data-ttu-id="91416-105">Описывает целочисленный вектор 4D.</span><span class="sxs-lookup"><span data-stu-id="91416-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="91416-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91416-106">Syntax</span></span>


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
```



## <a name="members"></a><span data-ttu-id="91416-107">Участники</span><span class="sxs-lookup"><span data-stu-id="91416-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="91416-108">**x**</span><span class="sxs-lookup"><span data-stu-id="91416-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="91416-109">компонент x вектора.</span><span class="sxs-lookup"><span data-stu-id="91416-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="91416-110">**y**</span><span class="sxs-lookup"><span data-stu-id="91416-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="91416-111">y-компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="91416-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="91416-112">**гармошкой**</span><span class="sxs-lookup"><span data-stu-id="91416-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="91416-113">z-компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="91416-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="91416-114">**w**</span><span class="sxs-lookup"><span data-stu-id="91416-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="91416-115">w — компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="91416-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91416-116">Требования</span><span class="sxs-lookup"><span data-stu-id="91416-116">Requirements</span></span>



| <span data-ttu-id="91416-117">Требование</span><span class="sxs-lookup"><span data-stu-id="91416-117">Requirement</span></span> | <span data-ttu-id="91416-118">Значение</span><span class="sxs-lookup"><span data-stu-id="91416-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91416-119">Header</span><span class="sxs-lookup"><span data-stu-id="91416-119">Header</span></span><br/> | <dl> <span data-ttu-id="91416-120"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="91416-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91416-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91416-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91416-122">Структуры</span><span class="sxs-lookup"><span data-stu-id="91416-122">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="91416-123">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="91416-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





