---
description: Содержит красную, зеленую и синюю данные пандуса.
ms.assetid: c596f47a-6c09-4b97-ab2f-b1da3d851aa4
title: Структура D3DGAMMARAMP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DGAMMARAMP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 496885b8267d339c7617ec24b884fa193f8d9945
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703845"
---
# <a name="d3dgammaramp-structure"></a><span data-ttu-id="b855e-103">Структура D3DGAMMARAMP</span><span class="sxs-lookup"><span data-stu-id="b855e-103">D3DGAMMARAMP structure</span></span>

<span data-ttu-id="b855e-104">Содержит красную, зеленую и синюю данные пандуса.</span><span class="sxs-lookup"><span data-stu-id="b855e-104">Contains red, green, and blue ramp data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b855e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b855e-105">Syntax</span></span>


```C++
typedef struct D3DGAMMARAMP {
  WORD red[256];
  WORD green[256];
  WORD blue[256];
} D3DGAMMARAMP, *LPD3DGAMMARAMP;
```



## <a name="members"></a><span data-ttu-id="b855e-106">Члены</span><span class="sxs-lookup"><span data-stu-id="b855e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b855e-107">**отмечен**</span><span class="sxs-lookup"><span data-stu-id="b855e-107">**red**</span></span>
</dt> <dd>

<span data-ttu-id="b855e-108">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b855e-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b855e-109">Массив элементов WORD 256, описывающих красный цвет гаммы.</span><span class="sxs-lookup"><span data-stu-id="b855e-109">Array of 256 WORD element that describes the red gamma ramp.</span></span>

</dd> <dt>

<span data-ttu-id="b855e-110">**зеленого**</span><span class="sxs-lookup"><span data-stu-id="b855e-110">**green**</span></span>
</dt> <dd>

<span data-ttu-id="b855e-111">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b855e-111">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b855e-112">Массив элементов WORD 256, описывающий зеленый цвет гаммы.</span><span class="sxs-lookup"><span data-stu-id="b855e-112">Array of 256 WORD element that describes the green gamma ramp.</span></span>

</dd> <dt>

<span data-ttu-id="b855e-113">**выделен**</span><span class="sxs-lookup"><span data-stu-id="b855e-113">**blue**</span></span>
</dt> <dd>

<span data-ttu-id="b855e-114">Тип: **[ **слово**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b855e-114">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b855e-115">Массив элементов WORD 256, описывающих синюю гамму цветов.</span><span class="sxs-lookup"><span data-stu-id="b855e-115">Array of 256 WORD element that describes the blue gamma ramp.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b855e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b855e-116">Requirements</span></span>



| <span data-ttu-id="b855e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b855e-117">Requirement</span></span> | <span data-ttu-id="b855e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b855e-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b855e-119">Header</span><span class="sxs-lookup"><span data-stu-id="b855e-119">Header</span></span><br/> | <dl> <span data-ttu-id="b855e-120"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b855e-120"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b855e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b855e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b855e-122">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="b855e-122">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="b855e-123">**жетгаммарамп**</span><span class="sxs-lookup"><span data-stu-id="b855e-123">**GetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
</dt> <dt>

[<span data-ttu-id="b855e-124">**сетгаммарамп**</span><span class="sxs-lookup"><span data-stu-id="b855e-124">**SetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
</dt> </dl>

 

 
