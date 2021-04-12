---
description: Вычисляет освещение, которое представляет собой конус с постоянной интенсивностью и возвращает Спектрал сферическую гармонию (SH) данных.
ms.assetid: ad2b9c86-cf1a-426e-88e6-4c543519e002
title: Функция D3DXSHEvalConeLight (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalConeLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 97bd700d1c38441db6c5e68554cf038d9081efaa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273914"
---
# <a name="d3dxshevalconelight-function-d3dx10h"></a><span data-ttu-id="c838a-103">Функция D3DXSHEvalConeLight (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="c838a-103">D3DXSHEvalConeLight function (D3DX10.h)</span></span>

<span data-ttu-id="c838a-104">Вычисляет освещение, которое представляет собой конус с постоянной интенсивностью и возвращает Спектрал сферическую гармонию (SH) данных.</span><span class="sxs-lookup"><span data-stu-id="c838a-104">Evaluates a light that is a cone of constant intensity and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c838a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c838a-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalConeLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="c838a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c838a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c838a-107">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c838a-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c838a-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c838a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c838a-109">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="c838a-109">Order of the SH evaluation.</span></span> <span data-ttu-id="c838a-110">Должен находиться в диапазоне от D3DXSH \_ минордер до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="c838a-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="c838a-111">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="c838a-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="c838a-112">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="c838a-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="c838a-113">*пдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c838a-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c838a-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c838a-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c838a-115">Указатель на вектор направления (x, y, z) полушари оси, в котором оцениваются функции-основания SH.</span><span class="sxs-lookup"><span data-stu-id="c838a-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="c838a-116">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="c838a-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c838a-117">*Радиус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c838a-117">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c838a-118">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c838a-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c838a-119">Радиус конуса в радианах.</span><span class="sxs-lookup"><span data-stu-id="c838a-119">Radius of cone in radians.</span></span>

</dd> <dt>

<span data-ttu-id="c838a-120">*Ринтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c838a-120">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c838a-121">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c838a-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c838a-122">Красная интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="c838a-122">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="c838a-123">*Гинтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c838a-123">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c838a-124">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c838a-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c838a-125">Зеленая интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="c838a-125">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="c838a-126">*Бинтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c838a-126">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c838a-127">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c838a-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c838a-128">Синяя интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="c838a-128">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="c838a-129">*Праут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c838a-129">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c838a-130">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c838a-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c838a-131">Указатель на выходной вектор SH для красного компонента.</span><span class="sxs-lookup"><span data-stu-id="c838a-131">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="c838a-132">*пгаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c838a-132">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c838a-133">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c838a-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c838a-134">Указатель на выходной вектор SH для зеленого компонента.</span><span class="sxs-lookup"><span data-stu-id="c838a-134">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="c838a-135">*пбаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c838a-135">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c838a-136">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c838a-136">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c838a-137">Указатель на выходной вектор SH для синего компонента.</span><span class="sxs-lookup"><span data-stu-id="c838a-137">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c838a-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c838a-138">Return value</span></span>

<span data-ttu-id="c838a-139">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c838a-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c838a-140">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c838a-140">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c838a-141">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="c838a-141">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c838a-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c838a-142">Remarks</span></span>

<span data-ttu-id="c838a-143">Вычисляет освещение, которое представляет собой конус с постоянной интенсивностью и возвращает Спектрал данные SH.</span><span class="sxs-lookup"><span data-stu-id="c838a-143">Evaluates a light that is a cone of constant intensity and returns spectral SH data.</span></span> <span data-ttu-id="c838a-144">Выходной вектор выдается таким образом, что если коэффициент интенсивности/G/B равен 1, радианце выхода точки непосредственно под светлой стороной (ориентированной на конусное направление на рассеянном объекте с албедоом 1) будет 1,0.</span><span class="sxs-lookup"><span data-stu-id="c838a-144">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the exit radiance of a point directly under the light (oriented in the cone direction on a diffuse object with an albedo of 1) would be 1.0.</span></span> <span data-ttu-id="c838a-145">Будет выполнено вычисление трех примеров Спектрал. Праут будет возвращен, тогда как Пгаут и Пбаут могут быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="c838a-145">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="c838a-146">В сфере с радиусом единицы, как показано на следующем рисунке, направление может быть задано просто с помощью тета, угла относительно оси z в правильном направлении, а значение фи — от z.</span><span class="sxs-lookup"><span data-stu-id="c838a-146">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![Иллюстрация сферы с радиусом единицы](images/spherical-coordinates.png)

<span data-ttu-id="c838a-148">В следующих уравнениях показана связь между координатами декартовы (x, y, z) и сферами (тета, фи) в единичной сфере.</span><span class="sxs-lookup"><span data-stu-id="c838a-148">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="c838a-149">Угол тета зависит от диапазона от 0 до 2 Пи, а значение фи отличается от 0 до PI.</span><span class="sxs-lookup"><span data-stu-id="c838a-149">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![формулы связи между декартовы и сферыми координатами](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="c838a-151">Требования</span><span class="sxs-lookup"><span data-stu-id="c838a-151">Requirements</span></span>



| <span data-ttu-id="c838a-152">Требование</span><span class="sxs-lookup"><span data-stu-id="c838a-152">Requirement</span></span> | <span data-ttu-id="c838a-153">Значение</span><span class="sxs-lookup"><span data-stu-id="c838a-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c838a-154">Header</span><span class="sxs-lookup"><span data-stu-id="c838a-154">Header</span></span><br/>  | <dl> <span data-ttu-id="c838a-155"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c838a-155"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c838a-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c838a-156">Library</span></span><br/> | <dl> <span data-ttu-id="c838a-157"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c838a-157"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c838a-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c838a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c838a-159">Математические функции</span><span class="sxs-lookup"><span data-stu-id="c838a-159">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
