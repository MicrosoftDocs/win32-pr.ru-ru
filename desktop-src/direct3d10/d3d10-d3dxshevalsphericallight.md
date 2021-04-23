---
description: Оценивает сферическую индикацию и возвращает Спектрал данные сферического гармонического (SH).
ms.assetid: e2a2b998-285a-46ef-99fe-ccc923013e9a
title: Функция D3DXSHEvalSphericalLight (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalSphericalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c658480a08360fe8489cfc86319a689e828c0a1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355583"
---
# <a name="d3dxshevalsphericallight-function-d3dx10h"></a><span data-ttu-id="18c30-103">Функция D3DXSHEvalSphericalLight (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="18c30-103">D3DXSHEvalSphericalLight function (D3DX10.h)</span></span>

<span data-ttu-id="18c30-104">Оценивает сферическую индикацию и возвращает Спектрал данные сферического гармонического (SH).</span><span class="sxs-lookup"><span data-stu-id="18c30-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="18c30-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18c30-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pPos,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="18c30-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="18c30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18c30-107">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18c30-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18c30-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18c30-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18c30-109">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="18c30-109">Order of the SH evaluation.</span></span> <span data-ttu-id="18c30-110">Должен находиться в диапазоне от D3DXSH \_ минордер до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="18c30-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="18c30-111">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="18c30-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="18c30-112">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="18c30-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="18c30-113">*ППОС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18c30-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18c30-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="18c30-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="18c30-115">Указатель на точку освещения.</span><span class="sxs-lookup"><span data-stu-id="18c30-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="18c30-116">*Радиус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18c30-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18c30-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18c30-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18c30-118">Радиус сферических источников освещения.</span><span class="sxs-lookup"><span data-stu-id="18c30-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="18c30-119">*Ринтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18c30-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18c30-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18c30-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18c30-121">Красная интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="18c30-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="18c30-122">*Гинтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18c30-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18c30-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18c30-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18c30-124">Зеленая интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="18c30-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="18c30-125">*Бинтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18c30-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18c30-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18c30-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18c30-127">Синяя интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="18c30-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="18c30-128">*Праут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18c30-128">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18c30-129">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="18c30-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="18c30-130">Указатель на выходной вектор SH для красного компонента.</span><span class="sxs-lookup"><span data-stu-id="18c30-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="18c30-131">*пгаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18c30-131">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18c30-132">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="18c30-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="18c30-133">Указатель на выходной вектор SH для зеленого компонента.</span><span class="sxs-lookup"><span data-stu-id="18c30-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="18c30-134">*пбаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18c30-134">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18c30-135">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="18c30-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="18c30-136">Указатель на выходной вектор SH для синего компонента.</span><span class="sxs-lookup"><span data-stu-id="18c30-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18c30-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18c30-137">Return value</span></span>

<span data-ttu-id="18c30-138">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="18c30-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="18c30-139">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="18c30-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="18c30-140">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="18c30-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="18c30-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18c30-141">Remarks</span></span>

<span data-ttu-id="18c30-142">Оценивает сферическую индикацию и возвращает Спектрал данные SH.</span><span class="sxs-lookup"><span data-stu-id="18c30-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="18c30-143">Не существует нормализации интенсивности света, подобного для направленного освещения, поэтому при указании интенситиес необходимо учитывать осторожность.</span><span class="sxs-lookup"><span data-stu-id="18c30-143">There is no normalization of the intensity of the light like there is for directional lights, so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="18c30-144">Будет выполнено вычисление трех примеров Спектрал. Праут будет возвращен, тогда как Пгаут и Пбаут могут быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="18c30-144">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="18c30-145">В сфере с радиусом единицы, как показано на следующем рисунке, направление может быть задано просто с помощью тета, угла относительно оси z в правильном направлении, а значение фи — от z.</span><span class="sxs-lookup"><span data-stu-id="18c30-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![Иллюстрация сферы с радиусом единицы](images/spherical-coordinates.png)

<span data-ttu-id="18c30-147">В следующих уравнениях показана связь между координатами декартовы (x, y, z) и сферами (тета, фи) в единичной сфере.</span><span class="sxs-lookup"><span data-stu-id="18c30-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="18c30-148">Угол тета зависит от диапазона от 0 до 2 Пи, а значение фи отличается от 0 до PI.</span><span class="sxs-lookup"><span data-stu-id="18c30-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![формулы связи между декартовы и сферыми координатами](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="18c30-150">Требования</span><span class="sxs-lookup"><span data-stu-id="18c30-150">Requirements</span></span>



| <span data-ttu-id="18c30-151">Требование</span><span class="sxs-lookup"><span data-stu-id="18c30-151">Requirement</span></span> | <span data-ttu-id="18c30-152">Значение</span><span class="sxs-lookup"><span data-stu-id="18c30-152">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18c30-153">Header</span><span class="sxs-lookup"><span data-stu-id="18c30-153">Header</span></span><br/>  | <dl> <span data-ttu-id="18c30-154"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="18c30-154"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="18c30-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="18c30-155">Library</span></span><br/> | <dl> <span data-ttu-id="18c30-156"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18c30-156"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18c30-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18c30-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18c30-158">Математические функции</span><span class="sxs-lookup"><span data-stu-id="18c30-158">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
