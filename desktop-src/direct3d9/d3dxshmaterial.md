---
description: В сферах с сферическими гармониями (SH) предварительно вычисленные радианце передаваемые материалы (PRT).
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: Структура D3DXSHMATERIAL (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 0600cc0c1ebe086f0d6679182125350b1ee8ca98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713645"
---
# <a name="d3dxshmaterial-structure"></a><span data-ttu-id="e0c07-103">Структура D3DXSHMATERIAL</span><span class="sxs-lookup"><span data-stu-id="e0c07-103">D3DXSHMATERIAL structure</span></span>

<span data-ttu-id="e0c07-104">В сферах с сферическими гармониями (SH) предварительно вычисленные радианце передаваемые материалы (PRT).</span><span class="sxs-lookup"><span data-stu-id="e0c07-104">Spherical harmonic (SH) precomputed radiance transfer (PRT) material characteristics.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0c07-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0c07-105">Syntax</span></span>


```C++
typedef struct D3DXSHMATERIAL {
  D3DCOLORVALUE Diffuse;
  BOOL          bMirror;
  BOOL          bSubSurf;
  FLOAT         RelativeIndexOfRefraction;
  D3DCOLORVALUE Absorption;
  D3DCOLORVALUE ReducedScattering;
} D3DXSHMATERIAL, *LPD3DXSHMATERIAL;
```



## <a name="members"></a><span data-ttu-id="e0c07-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e0c07-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e0c07-107">**Диффузное**</span><span class="sxs-lookup"><span data-stu-id="e0c07-107">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="e0c07-108">Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="e0c07-108">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e0c07-109">Рассеянный албедо поверхности.</span><span class="sxs-lookup"><span data-stu-id="e0c07-109">Diffuse albedo of the surface.</span></span> <span data-ttu-id="e0c07-110">Это значение игнорируется, если объект является зеркалом.</span><span class="sxs-lookup"><span data-stu-id="e0c07-110">This value is ignored if the object is a mirror.</span></span>

</dd> <dt>

<span data-ttu-id="e0c07-111">**бмиррор**</span><span class="sxs-lookup"><span data-stu-id="e0c07-111">**bMirror**</span></span>
</dt> <dd>

<span data-ttu-id="e0c07-112">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0c07-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e0c07-113">Необходимо задать значение **false**.</span><span class="sxs-lookup"><span data-stu-id="e0c07-113">Must be set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e0c07-114">**бсубсурф**</span><span class="sxs-lookup"><span data-stu-id="e0c07-114">**bSubSurf**</span></span>
</dt> <dd>

<span data-ttu-id="e0c07-115">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0c07-115">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e0c07-116">Задайте значение **true** , чтобы включить рассеивание подповерхности; любой объект, не являющийся разбросам подповерхности, не может быть зеркалом.</span><span class="sxs-lookup"><span data-stu-id="e0c07-116">Set to **TRUE** to enable subsurface scattering; any object that does subsurface scattering cannot be a mirror.</span></span>

</dd> <dt>

<span data-ttu-id="e0c07-117">**релативеиндексофрефрактион**</span><span class="sxs-lookup"><span data-stu-id="e0c07-117">**RelativeIndexOfRefraction**</span></span>
</dt> <dd>

<span data-ttu-id="e0c07-118">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0c07-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e0c07-119">Относительный индекс refraction является соотношением между двумя абсолютными индексами refraction.</span><span class="sxs-lookup"><span data-stu-id="e0c07-119">Relative index of refraction is the ratio between two absolute indexes of refraction.</span></span> <span data-ttu-id="e0c07-120">Индекс refraction — это отношение синуса угла объекта к синусу угла дробной части.</span><span class="sxs-lookup"><span data-stu-id="e0c07-120">An index of refraction is the ratio of the sine of the angle of incidence to the sine of the angle of refraction.</span></span>

</dd> <dt>

<span data-ttu-id="e0c07-121">**абсорптион**</span><span class="sxs-lookup"><span data-stu-id="e0c07-121">**Absorption**</span></span>
</dt> <dd>

<span data-ttu-id="e0c07-122">Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="e0c07-122">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e0c07-123">Коэффициент абсорптион — это параметр уравнения для подготовки к просмотру тома, который используется для моделирования облегчения распространения на принимающем носителе.</span><span class="sxs-lookup"><span data-stu-id="e0c07-123">The absorption coefficient is a parameter to the volume rendering equation used to model light propagation in a participating medium.</span></span>

</dd> <dt>

<span data-ttu-id="e0c07-124">**редуцедскаттеринг**</span><span class="sxs-lookup"><span data-stu-id="e0c07-124">**ReducedScattering**</span></span>
</dt> <dd>

<span data-ttu-id="e0c07-125">Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="e0c07-125">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e0c07-126">Уменьшение коэффициента распределения — это параметр уравнения для подготовки к просмотру тома, который используется для моделирования облегчения распространения на принимающем носителе.</span><span class="sxs-lookup"><span data-stu-id="e0c07-126">The reduced scattering coefficient is a parameter to the volume rendering equation used to model light propagation in a participating medium.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0c07-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0c07-127">Remarks</span></span>

<span data-ttu-id="e0c07-128">Спектрал сцены используют красный канал из материалов вместо значения светимости.</span><span class="sxs-lookup"><span data-stu-id="e0c07-128">Non-spectral scenes use the red channel from the materials instead of the luminance value.</span></span>

<span data-ttu-id="e0c07-129">Дополнительные сведения о PRT см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="e0c07-129">For more information about PRT see:</span></span>

-   <span data-ttu-id="e0c07-130">Йенсен, Хенрик ванн, et al. Сигграф материалы: практическая модель для транспорта тонкой поверхности, 2001.</span><span class="sxs-lookup"><span data-stu-id="e0c07-130">Jensen, Henrik Wann, et al. Siggraph Proceedings: A Practical Model for Subsurface Light Transport, 2001.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0c07-131">Требования</span><span class="sxs-lookup"><span data-stu-id="e0c07-131">Requirements</span></span>



| <span data-ttu-id="e0c07-132">Требование</span><span class="sxs-lookup"><span data-stu-id="e0c07-132">Requirement</span></span> | <span data-ttu-id="e0c07-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e0c07-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c07-134">Header</span><span class="sxs-lookup"><span data-stu-id="e0c07-134">Header</span></span><br/> | <dl> <span data-ttu-id="e0c07-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0c07-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0c07-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0c07-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0c07-137">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="e0c07-137">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
