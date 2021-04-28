---
description: Функция D3DXSHEvalConeLight (D3dx9math. h) — вычисляет освещение, которое представляет собой конус с постоянной интенсивностью и возвращает Спектрал сферическую гармонию (SH) данных.
ms.assetid: 13088e3b-76ae-43ef-886e-686f1f18a31d
title: Функция D3DXSHEvalConeLight (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31c90e705a0bb4e82813fff42673e143c5acf171
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117952"
---
# <a name="d3dxshevalconelight-function-d3dx9mathh"></a><span data-ttu-id="ed257-103">Функция D3DXSHEvalConeLight (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ed257-103">D3DXSHEvalConeLight function (D3dx9math.h)</span></span>

<span data-ttu-id="ed257-104">Вычисляет освещение, которое представляет собой конус с постоянной интенсивностью и возвращает Спектрал сферическую гармонию (SH) данных.</span><span class="sxs-lookup"><span data-stu-id="ed257-104">Evaluates a light that is a cone of constant intensity and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed257-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed257-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalConeLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="ed257-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed257-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed257-107">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed257-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed257-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed257-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed257-109">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="ed257-109">Order of the SH evaluation.</span></span> <span data-ttu-id="ed257-110">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="ed257-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="ed257-111">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="ed257-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="ed257-112">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="ed257-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="ed257-113">*пдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed257-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed257-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ed257-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ed257-115">Указатель на вектор направления (x, y, z) полушари оси, в котором оцениваются функции-основания SH.</span><span class="sxs-lookup"><span data-stu-id="ed257-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="ed257-116">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="ed257-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ed257-117">*Радиус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed257-117">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed257-118">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed257-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed257-119">Радиус конуса в радианах.</span><span class="sxs-lookup"><span data-stu-id="ed257-119">Radius of cone in radians.</span></span>

</dd> <dt>

<span data-ttu-id="ed257-120">*Ринтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed257-120">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed257-121">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed257-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed257-122">Красная интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="ed257-122">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="ed257-123">*Гинтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed257-123">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed257-124">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed257-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed257-125">Зеленая интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="ed257-125">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="ed257-126">*Бинтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed257-126">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed257-127">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed257-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed257-128">Синяя интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="ed257-128">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="ed257-129">*Праут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ed257-129">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed257-130">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed257-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ed257-131">Указатель на выходной вектор SH для красного компонента.</span><span class="sxs-lookup"><span data-stu-id="ed257-131">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="ed257-132">*пгаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ed257-132">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed257-133">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed257-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ed257-134">Указатель на выходной вектор SH для зеленого компонента.</span><span class="sxs-lookup"><span data-stu-id="ed257-134">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="ed257-135">*пбаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ed257-135">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed257-136">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed257-136">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ed257-137">Указатель на выходной вектор SH для синего компонента.</span><span class="sxs-lookup"><span data-stu-id="ed257-137">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed257-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed257-138">Return value</span></span>

<span data-ttu-id="ed257-139">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed257-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed257-140">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ed257-140">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ed257-141">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="ed257-141">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed257-142">Remarks</span><span class="sxs-lookup"><span data-stu-id="ed257-142">Remarks</span></span>

<span data-ttu-id="ed257-143">Вычисляет освещение, которое представляет собой конус с постоянной интенсивностью и возвращает Спектрал данные SH.</span><span class="sxs-lookup"><span data-stu-id="ed257-143">Evaluates a light that is a cone of constant intensity and returns spectral SH data.</span></span> <span data-ttu-id="ed257-144">Выходной вектор выдается таким образом, что если коэффициент интенсивности/G/B равен 1, радианце выхода точки непосредственно под светлой стороной (ориентированной на конусное направление на рассеянном объекте с албедоом 1) будет 1,0.</span><span class="sxs-lookup"><span data-stu-id="ed257-144">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the exit radiance of a point directly under the light (oriented in the cone direction on a diffuse object with an albedo of 1) would be 1.0.</span></span> <span data-ttu-id="ed257-145">Будет выполнено вычисление трех примеров Спектрал. *Праут* будет возвращен, тогда как *пгаут* и *пбаут* могут быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="ed257-145">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="ed257-146">В сфере с радиусом единицы, как показано на следующем рисунке, направление может быть задано просто с помощью тета, угла относительно оси z в [правильном направлении](coordinate-systems.md), а значение фи — от z.</span><span class="sxs-lookup"><span data-stu-id="ed257-146">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Иллюстрация сферы с радиусом единицы](images/spherical-coordinates.png)

<span data-ttu-id="ed257-148">В следующих уравнениях показана связь между координатами декартовы (x, y, z) и сферами (тета, фи) в единичной сфере.</span><span class="sxs-lookup"><span data-stu-id="ed257-148">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="ed257-149">Угол тета зависит от диапазона от 0 до 2 Пи, а значение фи отличается от 0 до PI.</span><span class="sxs-lookup"><span data-stu-id="ed257-149">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![формулы связи между декартовы и сферыми координатами](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="ed257-151">Требования</span><span class="sxs-lookup"><span data-stu-id="ed257-151">Requirements</span></span>



| <span data-ttu-id="ed257-152">Требование</span><span class="sxs-lookup"><span data-stu-id="ed257-152">Requirement</span></span> | <span data-ttu-id="ed257-153">Значение</span><span class="sxs-lookup"><span data-stu-id="ed257-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed257-154">Header</span><span class="sxs-lookup"><span data-stu-id="ed257-154">Header</span></span><br/>  | <dl> <span data-ttu-id="ed257-155"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed257-155"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ed257-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ed257-156">Library</span></span><br/> | <dl> <span data-ttu-id="ed257-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed257-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ed257-158">См. также</span><span class="sxs-lookup"><span data-stu-id="ed257-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed257-159">Математические функции</span><span class="sxs-lookup"><span data-stu-id="ed257-159">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ed257-160">Предварительно вычисленный перенос Радианце (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ed257-160">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
