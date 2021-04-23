---
description: Задает свойства материала.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: Структура D3DMATERIAL9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIAL9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b9c3ad93fe2cb80fe758e2e66da37cce9d4267ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424425"
---
# <a name="d3dmaterial9-structure"></a><span data-ttu-id="af3fe-103">Структура D3DMATERIAL9</span><span class="sxs-lookup"><span data-stu-id="af3fe-103">D3DMATERIAL9 structure</span></span>

<span data-ttu-id="af3fe-104">Задает свойства материала.</span><span class="sxs-lookup"><span data-stu-id="af3fe-104">Specifies material properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="af3fe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af3fe-105">Syntax</span></span>


```C++
typedef struct D3DMATERIAL9 {
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Ambient;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Emissive;
  float         Power;
} D3DMATERIAL9, *LPD3DMATERIAL9;
```



## <a name="members"></a><span data-ttu-id="af3fe-106">Члены</span><span class="sxs-lookup"><span data-stu-id="af3fe-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="af3fe-107">**Диффузное**</span><span class="sxs-lookup"><span data-stu-id="af3fe-107">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="af3fe-108">Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="af3fe-108">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="af3fe-109">Значение, указывающее рассеянный цвет материала.</span><span class="sxs-lookup"><span data-stu-id="af3fe-109">Value specifying the diffuse color of the material.</span></span> <span data-ttu-id="af3fe-110">См. [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="af3fe-110">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="af3fe-111">**Окружающее**</span><span class="sxs-lookup"><span data-stu-id="af3fe-111">**Ambient**</span></span>
</dt> <dd>

<span data-ttu-id="af3fe-112">Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="af3fe-112">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="af3fe-113">Значение, указывающее внешний цвет материала.</span><span class="sxs-lookup"><span data-stu-id="af3fe-113">Value specifying the ambient color of the material.</span></span> <span data-ttu-id="af3fe-114">См. [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="af3fe-114">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="af3fe-115">**Отражающее**</span><span class="sxs-lookup"><span data-stu-id="af3fe-115">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="af3fe-116">Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="af3fe-116">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="af3fe-117">Значение, указывающее отражающий цвет материала.</span><span class="sxs-lookup"><span data-stu-id="af3fe-117">Value specifying the specular color of the material.</span></span> <span data-ttu-id="af3fe-118">См. [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="af3fe-118">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="af3fe-119">**Эмиссионное**</span><span class="sxs-lookup"><span data-stu-id="af3fe-119">**Emissive**</span></span>
</dt> <dd>

<span data-ttu-id="af3fe-120">Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="af3fe-120">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="af3fe-121">Значение, указывающее цвет эмиссионный материала.</span><span class="sxs-lookup"><span data-stu-id="af3fe-121">Value specifying the emissive color of the material.</span></span> <span data-ttu-id="af3fe-122">См. [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="af3fe-122">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="af3fe-123">**Power**</span><span class="sxs-lookup"><span data-stu-id="af3fe-123">**Power**</span></span>
</dt> <dd>

<span data-ttu-id="af3fe-124">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="af3fe-124">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="af3fe-125">Значение с плавающей запятой, определяющее четкость отраженных светов.</span><span class="sxs-lookup"><span data-stu-id="af3fe-125">Floating-point value specifying the sharpness of specular highlights.</span></span> <span data-ttu-id="af3fe-126">Чем выше значение, тем четче выделение.</span><span class="sxs-lookup"><span data-stu-id="af3fe-126">The higher the value, the sharper the highlight.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af3fe-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af3fe-127">Remarks</span></span>

<span data-ttu-id="af3fe-128">Чтобы отключить отраженные блики, присвойте параметру D3DRS \_ Спекуларенабле **значение false**, используя [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="af3fe-128">To turn off specular highlights, set D3DRS\_SPECULARENABLE to **FALSE**, using [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span> <span data-ttu-id="af3fe-129">Это самый быстрый вариант, так как отраженные блики не будут вычисляться.</span><span class="sxs-lookup"><span data-stu-id="af3fe-129">This is the fastest option because no specular highlights will be calculated.</span></span>

<span data-ttu-id="af3fe-130">Дополнительные сведения об использовании механизма освещения для вычисления отраженного освещения см. в разделе [Зеркальное освещение (Direct3D 9)](specular-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="af3fe-130">For more information about using the lighting engine to calculate specular lighting, see [Specular Lighting (Direct3D 9)](specular-lighting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af3fe-131">Требования</span><span class="sxs-lookup"><span data-stu-id="af3fe-131">Requirements</span></span>



| <span data-ttu-id="af3fe-132">Требование</span><span class="sxs-lookup"><span data-stu-id="af3fe-132">Requirement</span></span> | <span data-ttu-id="af3fe-133">Значение</span><span class="sxs-lookup"><span data-stu-id="af3fe-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af3fe-134">Header</span><span class="sxs-lookup"><span data-stu-id="af3fe-134">Header</span></span><br/> | <dl> <span data-ttu-id="af3fe-135"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="af3fe-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af3fe-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af3fe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af3fe-137">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="af3fe-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="af3fe-138">**IDirect3DDevice9:: о.**</span><span class="sxs-lookup"><span data-stu-id="af3fe-138">**IDirect3DDevice9::GetMaterial**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[<span data-ttu-id="af3fe-139">**IDirect3DDevice9:: Сетматериал**</span><span class="sxs-lookup"><span data-stu-id="af3fe-139">**IDirect3DDevice9::SetMaterial**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
