---
description: Функция D3DXSHEvalSphericalLight (D3dx9math. h) — оценивает сферическую освещенность и возвращает Спектрал сферическую гармонию (SH) данных.
ms.assetid: aa46c162-9c2d-49c0-925c-d0c06456f918
title: Функция D3DXSHEvalSphericalLight (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db671d58806d999e07b1aac1e8e4da2fb38acc6f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117892"
---
# <a name="d3dxshevalsphericallight-function-d3dx9mathh"></a><span data-ttu-id="48631-103">Функция D3DXSHEvalSphericalLight (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="48631-103">D3DXSHEvalSphericalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="48631-104">Оценивает сферическую индикацию и возвращает Спектрал данные сферического гармонического (SH).</span><span class="sxs-lookup"><span data-stu-id="48631-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="48631-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48631-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pPos,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="48631-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="48631-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48631-107">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48631-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48631-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48631-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48631-109">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="48631-109">Order of the SH evaluation.</span></span> <span data-ttu-id="48631-110">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="48631-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="48631-111">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="48631-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="48631-112">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="48631-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="48631-113">*ППОС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48631-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48631-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="48631-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="48631-115">Указатель на точку освещения.</span><span class="sxs-lookup"><span data-stu-id="48631-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="48631-116">*Радиус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48631-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48631-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48631-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48631-118">Радиус сферических источников освещения.</span><span class="sxs-lookup"><span data-stu-id="48631-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="48631-119">*Ринтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48631-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48631-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48631-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48631-121">Красная интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="48631-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="48631-122">*Гинтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48631-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48631-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48631-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48631-124">Зеленая интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="48631-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="48631-125">*Бинтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48631-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48631-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48631-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48631-127">Синяя интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="48631-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="48631-128">*Праут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="48631-128">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48631-129">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="48631-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="48631-130">Указатель на выходной вектор SH для красного компонента.</span><span class="sxs-lookup"><span data-stu-id="48631-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="48631-131">*пгаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="48631-131">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48631-132">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="48631-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="48631-133">Указатель на выходной вектор SH для зеленого компонента.</span><span class="sxs-lookup"><span data-stu-id="48631-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="48631-134">*пбаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="48631-134">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48631-135">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="48631-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="48631-136">Указатель на выходной вектор SH для синего компонента.</span><span class="sxs-lookup"><span data-stu-id="48631-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48631-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48631-137">Return value</span></span>

<span data-ttu-id="48631-138">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="48631-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="48631-139">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="48631-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="48631-140">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="48631-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="48631-141">Remarks</span><span class="sxs-lookup"><span data-stu-id="48631-141">Remarks</span></span>

<span data-ttu-id="48631-142">Оценивает сферическую индикацию и возвращает Спектрал данные SH.</span><span class="sxs-lookup"><span data-stu-id="48631-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="48631-143">Не существует нормализации интенсивности света, подобного для [направленного освещения](light-types.md), поэтому при указании интенситиес необходимо учитывать осторожность.</span><span class="sxs-lookup"><span data-stu-id="48631-143">There is no normalization of the intensity of the light like there is for [directional lights](light-types.md), so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="48631-144">Будет выполнено вычисление трех примеров Спектрал. *Праут* будет возвращен, тогда как *пгаут* и *пбаут* могут быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="48631-144">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="48631-145">В сфере с радиусом единицы, как показано на следующем рисунке, направление может быть задано просто с помощью тета, угла относительно оси z в [правильном направлении](coordinate-systems.md), а значение фи — от z.</span><span class="sxs-lookup"><span data-stu-id="48631-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Иллюстрация сферы с радиусом единицы](images/spherical-coordinates.png)

<span data-ttu-id="48631-147">В следующих уравнениях показана связь между координатами декартовы (x, y, z) и сферами (тета, фи) в единичной сфере.</span><span class="sxs-lookup"><span data-stu-id="48631-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="48631-148">Угол тета зависит от диапазона от 0 до 2 Пи, а значение фи отличается от 0 до PI.</span><span class="sxs-lookup"><span data-stu-id="48631-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![формулы связи между декартовы и сферыми координатами](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="48631-150">Требования</span><span class="sxs-lookup"><span data-stu-id="48631-150">Requirements</span></span>



| <span data-ttu-id="48631-151">Требование</span><span class="sxs-lookup"><span data-stu-id="48631-151">Requirement</span></span> | <span data-ttu-id="48631-152">Значение</span><span class="sxs-lookup"><span data-stu-id="48631-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48631-153">Header</span><span class="sxs-lookup"><span data-stu-id="48631-153">Header</span></span><br/>  | <dl> <span data-ttu-id="48631-154"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="48631-154"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="48631-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="48631-155">Library</span></span><br/> | <dl> <span data-ttu-id="48631-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48631-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="48631-157">См. также</span><span class="sxs-lookup"><span data-stu-id="48631-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48631-158">Математические функции</span><span class="sxs-lookup"><span data-stu-id="48631-158">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="48631-159">Предварительно вычисленный перенос Радианце (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="48631-159">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
