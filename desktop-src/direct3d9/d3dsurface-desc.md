---
description: Описывает поверхность.
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: Структура D3DSURFACE_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSURFACE_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6424bbe9b78532657670bc5cd9ad0705de89a3b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713595"
---
# <a name="d3dsurface_desc-structure"></a><span data-ttu-id="e2a8c-103">\_Структура D3DSURFACE DESC</span><span class="sxs-lookup"><span data-stu-id="e2a8c-103">D3DSURFACE\_DESC structure</span></span>

<span data-ttu-id="e2a8c-104">Описывает поверхность.</span><span class="sxs-lookup"><span data-stu-id="e2a8c-104">Describes a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2a8c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2a8c-105">Syntax</span></span>


```C++
typedef struct D3DSURFACE_DESC {
  D3DFORMAT           Format;
  D3DRESOURCETYPE     Type;
  DWORD               Usage;
  D3DPOOL             Pool;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  UINT                Width;
  UINT                Height;
} D3DSURFACE_DESC, *LPD3DSURFACE_DESC;
```



## <a name="members"></a><span data-ttu-id="e2a8c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e2a8c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e2a8c-107">**Формат**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="e2a8c-108">Тип: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e2a8c-109">Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий формат поверхности.</span><span class="sxs-lookup"><span data-stu-id="e2a8c-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format.</span></span>

</dd> <dt>

<span data-ttu-id="e2a8c-110">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="e2a8c-111">Тип: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e2a8c-112">Член перечислимого типа [**D3DRESOURCETYPE**](./d3dresourcetype.md) , который определяет этот ресурс как поверхность.</span><span class="sxs-lookup"><span data-stu-id="e2a8c-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a surface.</span></span>

</dd> <dt>

<span data-ttu-id="e2a8c-113">**Использование**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="e2a8c-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e2a8c-115">Значение D3DUSAGE \_ депсстенЦил или D3DUSAGE \_ рендертаржет.</span><span class="sxs-lookup"><span data-stu-id="e2a8c-115">Either the D3DUSAGE\_DEPTHSTENCIL or D3DUSAGE\_RENDERTARGET values.</span></span> <span data-ttu-id="e2a8c-116">Дополнительные сведения см. в разделе [**D3DUSAGE**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="e2a8c-116">For more information, see [**D3DUSAGE**](d3dusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2a8c-117">**Пул.**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-117">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="e2a8c-118">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-118">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e2a8c-119">Член перечисляемого типа [**D3DPOOL**](./d3dpool.md) , указывающий класс памяти, выделенной для этой поверхности.</span><span class="sxs-lookup"><span data-stu-id="e2a8c-119">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this surface.</span></span>

</dd> <dt>

<span data-ttu-id="e2a8c-120">**мултисамплетипе**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-120">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="e2a8c-121">Тип: **[ **D3DMULTISAMPLE \_ тип**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-121">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e2a8c-122">Член перечисляемого [**типа \_ D3DMULTISAMPLE**](./d3dmultisample-type.md) , указывающий уровни многофакторной множественной выборки, поддерживаемые поверхностью.</span><span class="sxs-lookup"><span data-stu-id="e2a8c-122">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type, specifying the levels of full-scene multisampling supported by the surface.</span></span>

</dd> <dt>

<span data-ttu-id="e2a8c-123">**мултисамплекуалити**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-123">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="e2a8c-124">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e2a8c-125">Уровень качества.</span><span class="sxs-lookup"><span data-stu-id="e2a8c-125">Quality level.</span></span> <span data-ttu-id="e2a8c-126">Диапазон допустимых значений — от нуля до уровня, возвращенного Пкуалитилевелс, используемым [**чеккдевицемултисамплетипе**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span><span class="sxs-lookup"><span data-stu-id="e2a8c-126">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span></span> <span data-ttu-id="e2a8c-127">При передаче большего значения возвращается ошибка D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="e2a8c-127">Passing a larger value returns the error, D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="e2a8c-128">Значения Мултисамплекуалити для парных целевых объектов рендеринга, поверхности трафарета глубины и типа "многопримерные" должны соответствовать всем.</span><span class="sxs-lookup"><span data-stu-id="e2a8c-128">The MultisampleQuality values of paired render targets, depth stencil surfaces and the MultiSample type must all match.</span></span>

</dd> <dt>

<span data-ttu-id="e2a8c-129">**Width**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-129">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="e2a8c-130">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e2a8c-131">Ширина поверхности (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="e2a8c-131">Width of the surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e2a8c-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-132">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="e2a8c-133">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e2a8c-134">Высота поверхности (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="e2a8c-134">Height of the surface, in pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2a8c-135">Требования</span><span class="sxs-lookup"><span data-stu-id="e2a8c-135">Requirements</span></span>



| <span data-ttu-id="e2a8c-136">Требование</span><span class="sxs-lookup"><span data-stu-id="e2a8c-136">Requirement</span></span> | <span data-ttu-id="e2a8c-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e2a8c-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a8c-138">Header</span><span class="sxs-lookup"><span data-stu-id="e2a8c-138">Header</span></span><br/> | <dl> <span data-ttu-id="e2a8c-139"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2a8c-139"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2a8c-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2a8c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a8c-141">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="e2a8c-141">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="e2a8c-142">**жетлевелдеск**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-142">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[<span data-ttu-id="e2a8c-143">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-143">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[<span data-ttu-id="e2a8c-144">**жетлевелдеск**</span><span class="sxs-lookup"><span data-stu-id="e2a8c-144">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
