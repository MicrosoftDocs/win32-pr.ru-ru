---
description: Описывает состояние растрового изображения.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: Структура D3DRASTER_STATUS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRASTER_STATUS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e77ab0e6ee164eadae862ed03df5652c21ba7040
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703832"
---
# <a name="d3draster_status-structure"></a><span data-ttu-id="7a48c-103">\_Структура состояния D3DRASTER</span><span class="sxs-lookup"><span data-stu-id="7a48c-103">D3DRASTER\_STATUS structure</span></span>

<span data-ttu-id="7a48c-104">Описывает состояние растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="7a48c-104">Describes the raster status.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a48c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a48c-105">Syntax</span></span>


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a><span data-ttu-id="7a48c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="7a48c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a48c-107">**инвбланк**</span><span class="sxs-lookup"><span data-stu-id="7a48c-107">**InVBlank**</span></span>
</dt> <dd>

<span data-ttu-id="7a48c-108">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a48c-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a48c-109">**Значение true** , если точечный символ находится в вертикальной пустой точке.</span><span class="sxs-lookup"><span data-stu-id="7a48c-109">**TRUE** if the raster is in the vertical blank period.</span></span> <span data-ttu-id="7a48c-110">**Значение false** , если точечный символ не находится в вертикальной пустой точке.</span><span class="sxs-lookup"><span data-stu-id="7a48c-110">**FALSE** if the raster is not in the vertical blank period.</span></span>

</dd> <dt>

<span data-ttu-id="7a48c-111">**сканлине**</span><span class="sxs-lookup"><span data-stu-id="7a48c-111">**ScanLine**</span></span>
</dt> <dd>

<span data-ttu-id="7a48c-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a48c-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7a48c-113">Если Инвбланк имеет значение **false**, то это значение представляет собой целое число, приблизительно соответствующее текущей строке сканирования, закрашенной растровым.</span><span class="sxs-lookup"><span data-stu-id="7a48c-113">If InVBlank is **FALSE**, then this value is an integer roughly corresponding to the current scan line painted by the raster.</span></span> <span data-ttu-id="7a48c-114">Строки сканирования нумеруются так же, как координаты поверхности Direct3D: 0 — верхняя часть основной поверхности, расширение до значения (высота поверхности-1) в нижней части экрана.</span><span class="sxs-lookup"><span data-stu-id="7a48c-114">Scan lines are numbered in the same way as Direct3D surface coordinates: 0 is the top of the primary surface, extending to the value (height of the surface - 1) at the bottom of the display.</span></span>

<span data-ttu-id="7a48c-115">Если Инвбланк имеет значение **true**, то это значение устанавливается равным нулю и может быть пропущено.</span><span class="sxs-lookup"><span data-stu-id="7a48c-115">If InVBlank is **TRUE**, then this value is set to zero and can be ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a48c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7a48c-116">Requirements</span></span>



| <span data-ttu-id="7a48c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7a48c-117">Requirement</span></span> | <span data-ttu-id="7a48c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7a48c-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a48c-119">Header</span><span class="sxs-lookup"><span data-stu-id="7a48c-119">Header</span></span><br/> | <dl> <span data-ttu-id="7a48c-120"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a48c-120"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a48c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a48c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a48c-122">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="7a48c-122">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="7a48c-123">**жетрастерстатус**</span><span class="sxs-lookup"><span data-stu-id="7a48c-123">**GetRasterStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
