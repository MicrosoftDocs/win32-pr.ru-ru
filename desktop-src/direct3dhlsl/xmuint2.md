---
title: Структура XMUINT2
description: Описывает двумерный вектор целых чисел без знака.
ms.assetid: 8622eca1-fc8f-4129-a375-142b4f4018b0
keywords:
- HLSL структура XMUINT2
topic_type:
- apiref
api_name:
- XMUINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73d14bd43ec3b75a2bf503b7d742b6c69881475b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986768"
---
# <a name="xmuint2-structure"></a><span data-ttu-id="3283c-104">Структура XMUINT2</span><span class="sxs-lookup"><span data-stu-id="3283c-104">XMUINT2 structure</span></span>

<span data-ttu-id="3283c-105">Описывает двумерный вектор целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="3283c-105">Describes an 2D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="3283c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3283c-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT2 {
  UINT x;
  UINT y;
} XMUINT2;
```



## <a name="members"></a><span data-ttu-id="3283c-107">Участники</span><span class="sxs-lookup"><span data-stu-id="3283c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3283c-108">**x**</span><span class="sxs-lookup"><span data-stu-id="3283c-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="3283c-109">компонент x вектора.</span><span class="sxs-lookup"><span data-stu-id="3283c-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="3283c-110">**y**</span><span class="sxs-lookup"><span data-stu-id="3283c-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="3283c-111">y-компонент вектора.</span><span class="sxs-lookup"><span data-stu-id="3283c-111">y-component of the vector.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3283c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="3283c-112">Requirements</span></span>



| <span data-ttu-id="3283c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="3283c-113">Requirement</span></span> | <span data-ttu-id="3283c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3283c-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3283c-115">Header</span><span class="sxs-lookup"><span data-stu-id="3283c-115">Header</span></span><br/> | <dl> <span data-ttu-id="3283c-116"><dt>D3DX \_ дксгиформатконверт. inl</dt></span><span class="sxs-lookup"><span data-stu-id="3283c-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3283c-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3283c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3283c-118">Структуры</span><span class="sxs-lookup"><span data-stu-id="3283c-118">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="3283c-119">Распаковка и \_ формат упаковки для редактирования образа In-Place</span><span class="sxs-lookup"><span data-stu-id="3283c-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





