---
description: Определяет набор свойств освещения.
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: Структура D3DLIGHT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 90e72fbb2bf4f1d74a74dc177346387b36eb25e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273833"
---
# <a name="d3dlight9-structure"></a><span data-ttu-id="d3190-103">Структура D3DLIGHT9</span><span class="sxs-lookup"><span data-stu-id="d3190-103">D3DLIGHT9 structure</span></span>

<span data-ttu-id="d3190-104">Определяет набор свойств освещения.</span><span class="sxs-lookup"><span data-stu-id="d3190-104">Defines a set of lighting properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3190-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3190-105">Syntax</span></span>


```C++
typedef struct D3DLIGHT9 {
  D3DLIGHTTYPE  Type;
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Ambient;
  D3DVECTOR     Position;
  D3DVECTOR     Direction;
  float         Range;
  float         Falloff;
  float         Attenuation0;
  float         Attenuation1;
  float         Attenuation2;
  float         Theta;
  float         Phi;
} D3DLIGHT9, *LPD3DLIGHT;
```



## <a name="members"></a><span data-ttu-id="d3190-106">Члены</span><span class="sxs-lookup"><span data-stu-id="d3190-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d3190-107">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d3190-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="d3190-108">Тип: **[ **D3DLIGHTTYPE**](./d3dlighttype.md)**</span><span class="sxs-lookup"><span data-stu-id="d3190-108">Type: **[**D3DLIGHTTYPE**](./d3dlighttype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d3190-109">Тип источника освещения.</span><span class="sxs-lookup"><span data-stu-id="d3190-109">Type of the light source.</span></span> <span data-ttu-id="d3190-110">Это значение является одним из элементов перечисляемого типа [**D3DLIGHTTYPE**](./d3dlighttype.md) .</span><span class="sxs-lookup"><span data-stu-id="d3190-110">This value is one of the members of the [**D3DLIGHTTYPE**](./d3dlighttype.md) enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="d3190-111">**Диффузное**</span><span class="sxs-lookup"><span data-stu-id="d3190-111">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="d3190-112">Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="d3190-112">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d3190-113">Рассеянный цвет, выдаваемый источником света.</span><span class="sxs-lookup"><span data-stu-id="d3190-113">Diffuse color emitted by the light.</span></span> <span data-ttu-id="d3190-114">Этот элемент является структурой [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d3190-114">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d3190-115">**Отражающее**</span><span class="sxs-lookup"><span data-stu-id="d3190-115">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="d3190-116">Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="d3190-116">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d3190-117">Отражающий цвет, порожденный светом.</span><span class="sxs-lookup"><span data-stu-id="d3190-117">Specular color emitted by the light.</span></span> <span data-ttu-id="d3190-118">Этот элемент является структурой [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d3190-118">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d3190-119">**Окружающее**</span><span class="sxs-lookup"><span data-stu-id="d3190-119">**Ambient**</span></span>
</dt> <dd>

<span data-ttu-id="d3190-120">Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="d3190-120">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d3190-121">Окружающий цвет, выдаваемый источником освещения.</span><span class="sxs-lookup"><span data-stu-id="d3190-121">Ambient color emitted by the light.</span></span> <span data-ttu-id="d3190-122">Этот элемент является структурой [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d3190-122">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d3190-123">**Позиция**</span><span class="sxs-lookup"><span data-stu-id="d3190-123">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="d3190-124">Тип: **[ **D3DVECTOR**](d3dvector.md)**</span><span class="sxs-lookup"><span data-stu-id="d3190-124">Type: **[**D3DVECTOR**](d3dvector.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d3190-125">Расположение света в мировом пространстве, определяемое структурой [**D3DVECTOR**](d3dvector.md) .</span><span class="sxs-lookup"><span data-stu-id="d3190-125">Position of the light in world space, specified by a [**D3DVECTOR**](d3dvector.md) structure.</span></span> <span data-ttu-id="d3190-126">Этот член не имеет смысла для направленного освещения и в этом случае игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d3190-126">This member has no meaning for directional lights and is ignored in that case.</span></span>

</dd> <dt>

<span data-ttu-id="d3190-127">**Направление**</span><span class="sxs-lookup"><span data-stu-id="d3190-127">**Direction**</span></span>
</dt> <dd>

<span data-ttu-id="d3190-128">Тип: **[ **D3DVECTOR**](d3dvector.md)**</span><span class="sxs-lookup"><span data-stu-id="d3190-128">Type: **[**D3DVECTOR**](d3dvector.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d3190-129">Направление, указывающее, что источник света указывает на мировое пространство, заданное структурой [**D3DVECTOR**](d3dvector.md) .</span><span class="sxs-lookup"><span data-stu-id="d3190-129">Direction that the light is pointing in world space, specified by a [**D3DVECTOR**](d3dvector.md) structure.</span></span> <span data-ttu-id="d3190-130">Этот элемент имеет значение только для направленного и прожектора.</span><span class="sxs-lookup"><span data-stu-id="d3190-130">This member has meaning only for directional and spotlights.</span></span> <span data-ttu-id="d3190-131">Этот вектор не требует нормализации, но он должен иметь ненулевую длину.</span><span class="sxs-lookup"><span data-stu-id="d3190-131">This vector need not be normalized, but it should have a nonzero length.</span></span>

</dd> <dt>

<span data-ttu-id="d3190-132">**Диапазон**</span><span class="sxs-lookup"><span data-stu-id="d3190-132">**Range**</span></span>
</dt> <dd>

<span data-ttu-id="d3190-133">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d3190-133">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="d3190-134">Расстояние, за пределами которого освещение не имеет силы.</span><span class="sxs-lookup"><span data-stu-id="d3190-134">Distance beyond which the light has no effect.</span></span> <span data-ttu-id="d3190-135">Максимальное допустимое значение для этого элемента — квадратный корень из ФЛТ \_ Max.</span><span class="sxs-lookup"><span data-stu-id="d3190-135">The maximum allowable value for this member is the square root of FLT\_MAX.</span></span> <span data-ttu-id="d3190-136">Этот элемент не влияет на направленный свет.</span><span class="sxs-lookup"><span data-stu-id="d3190-136">This member does not affect directional lights.</span></span>

</dd> <dt>

<span data-ttu-id="d3190-137">**Переходят**</span><span class="sxs-lookup"><span data-stu-id="d3190-137">**Falloff**</span></span>
</dt> <dd>

<span data-ttu-id="d3190-138">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d3190-138">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="d3190-139">Уменьшите освещения между внутренним конусом прожектора (угол, заданный параметром тета) и внешним краями внешнего конуса (угол, заданный параметром фи).</span><span class="sxs-lookup"><span data-stu-id="d3190-139">Decrease in illumination between a spotlight's inner cone (the angle specified by Theta) and the outer edge of the outer cone (the angle specified by Phi).</span></span>

<span data-ttu-id="d3190-140">Воздействие спада на освещение незаметно.</span><span class="sxs-lookup"><span data-stu-id="d3190-140">The effect of falloff on the lighting is subtle.</span></span> <span data-ttu-id="d3190-141">Более того, при формировании кривой рассеивания начисляются небольшие потери производительности.</span><span class="sxs-lookup"><span data-stu-id="d3190-141">Furthermore, a small performance penalty is incurred by shaping the falloff curve.</span></span> <span data-ttu-id="d3190-142">По этим причинам большинство разработчиков устанавливают это значение равным 1,0.</span><span class="sxs-lookup"><span data-stu-id="d3190-142">For these reasons, most developers set this value to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="d3190-143">**Attenuation0**</span><span class="sxs-lookup"><span data-stu-id="d3190-143">**Attenuation0**</span></span>
</dt> <dd>

<span data-ttu-id="d3190-144">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d3190-144">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="d3190-145">Значение, указывающее, как интенсивность освещения изменяется по расстоянию.</span><span class="sxs-lookup"><span data-stu-id="d3190-145">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="d3190-146">Значения затухания игнорируются для направленного освещения.</span><span class="sxs-lookup"><span data-stu-id="d3190-146">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="d3190-147">Этот элемент представляет константу затухания.</span><span class="sxs-lookup"><span data-stu-id="d3190-147">This member represents an attenuation constant.</span></span> <span data-ttu-id="d3190-148">Сведения о ослаблении см. в разделе [Свойства освещения (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d3190-148">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="d3190-149">Допустимые значения для этого элемента в диапазоне от 0,0 до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="d3190-149">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="d3190-150">Для ненаправленного освещения все три значения затухания не должны быть установлены равными 0,0 одновременно.</span><span class="sxs-lookup"><span data-stu-id="d3190-150">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="d3190-151">**Attenuation1**</span><span class="sxs-lookup"><span data-stu-id="d3190-151">**Attenuation1**</span></span>
</dt> <dd>

<span data-ttu-id="d3190-152">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d3190-152">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="d3190-153">Значение, указывающее, как интенсивность освещения изменяется по расстоянию.</span><span class="sxs-lookup"><span data-stu-id="d3190-153">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="d3190-154">Значения затухания игнорируются для направленного освещения.</span><span class="sxs-lookup"><span data-stu-id="d3190-154">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="d3190-155">Этот элемент представляет константу затухания.</span><span class="sxs-lookup"><span data-stu-id="d3190-155">This member represents an attenuation constant.</span></span> <span data-ttu-id="d3190-156">Сведения о ослаблении см. в разделе [Свойства освещения (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d3190-156">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="d3190-157">Допустимые значения для этого элемента в диапазоне от 0,0 до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="d3190-157">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="d3190-158">Для ненаправленного освещения все три значения затухания не должны быть установлены равными 0,0 одновременно.</span><span class="sxs-lookup"><span data-stu-id="d3190-158">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="d3190-159">**Attenuation2**</span><span class="sxs-lookup"><span data-stu-id="d3190-159">**Attenuation2**</span></span>
</dt> <dd>

<span data-ttu-id="d3190-160">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d3190-160">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="d3190-161">Значение, указывающее, как интенсивность освещения изменяется по расстоянию.</span><span class="sxs-lookup"><span data-stu-id="d3190-161">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="d3190-162">Значения затухания игнорируются для направленного освещения.</span><span class="sxs-lookup"><span data-stu-id="d3190-162">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="d3190-163">Этот элемент представляет константу затухания.</span><span class="sxs-lookup"><span data-stu-id="d3190-163">This member represents an attenuation constant.</span></span> <span data-ttu-id="d3190-164">Сведения о ослаблении см. в разделе [Свойства освещения (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d3190-164">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="d3190-165">Допустимые значения для этого элемента в диапазоне от 0,0 до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="d3190-165">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="d3190-166">Для ненаправленного освещения все три значения затухания не должны быть установлены равными 0,0 одновременно.</span><span class="sxs-lookup"><span data-stu-id="d3190-166">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="d3190-167">**Тета-**</span><span class="sxs-lookup"><span data-stu-id="d3190-167">**Theta**</span></span>
</dt> <dd>

<span data-ttu-id="d3190-168">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d3190-168">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="d3190-169">Угол в радианах для внутреннего конуса прожектора, то есть полностью освещенный прожектор.</span><span class="sxs-lookup"><span data-stu-id="d3190-169">Angle, in radians, of a spotlight's inner cone - that is, the fully illuminated spotlight cone.</span></span> <span data-ttu-id="d3190-170">Это значение должно находиться в диапазоне от 0 до значения, заданного параметром фи.</span><span class="sxs-lookup"><span data-stu-id="d3190-170">This value must be in the range from 0 through the value specified by Phi.</span></span>

</dd> <dt>

<span data-ttu-id="d3190-171">**Фи**</span><span class="sxs-lookup"><span data-stu-id="d3190-171">**Phi**</span></span>
</dt> <dd>

<span data-ttu-id="d3190-172">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d3190-172">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="d3190-173">Угол в радианах, определяющий внешнее ребро внешнего конуса прожектора.</span><span class="sxs-lookup"><span data-stu-id="d3190-173">Angle, in radians, defining the outer edge of the spotlight's outer cone.</span></span> <span data-ttu-id="d3190-174">Точки за пределами этой конуса не освещены в центре внимания.</span><span class="sxs-lookup"><span data-stu-id="d3190-174">Points outside this cone are not lit by the spotlight.</span></span> <span data-ttu-id="d3190-175">Это значение должно находиться в диапазоне от 0 до PI.</span><span class="sxs-lookup"><span data-stu-id="d3190-175">This value must be between 0 and pi.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3190-176">Требования</span><span class="sxs-lookup"><span data-stu-id="d3190-176">Requirements</span></span>



| <span data-ttu-id="d3190-177">Требование</span><span class="sxs-lookup"><span data-stu-id="d3190-177">Requirement</span></span> | <span data-ttu-id="d3190-178">Значение</span><span class="sxs-lookup"><span data-stu-id="d3190-178">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3190-179">Header</span><span class="sxs-lookup"><span data-stu-id="d3190-179">Header</span></span><br/> | <dl> <span data-ttu-id="d3190-180"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3190-180"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3190-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3190-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3190-182">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="d3190-182">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d3190-183">**Легкая**</span><span class="sxs-lookup"><span data-stu-id="d3190-183">**GetLight**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[<span data-ttu-id="d3190-184">**сетлигхт**</span><span class="sxs-lookup"><span data-stu-id="d3190-184">**SetLight**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 
