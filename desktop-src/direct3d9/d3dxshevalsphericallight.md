---
description: Оценивает сферическую индикацию и возвращает Спектрал данные сферического гармонического (SH).
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
ms.openlocfilehash: 8581b4284e270b6df587be1a71fcf11f29c843d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354620"
---
# <a name="d3dxshevalsphericallight-function-d3dx9mathh"></a><span data-ttu-id="a82dc-103">Функция D3DXSHEvalSphericalLight (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a82dc-103">D3DXSHEvalSphericalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="a82dc-104">Оценивает сферическую индикацию и возвращает Спектрал данные сферического гармонического (SH).</span><span class="sxs-lookup"><span data-stu-id="a82dc-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a82dc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a82dc-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a82dc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a82dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a82dc-107">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a82dc-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a82dc-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a82dc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a82dc-109">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="a82dc-109">Order of the SH evaluation.</span></span> <span data-ttu-id="a82dc-110">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="a82dc-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="a82dc-111">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="a82dc-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="a82dc-112">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="a82dc-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="a82dc-113">*ППОС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a82dc-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a82dc-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a82dc-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a82dc-115">Указатель на точку освещения.</span><span class="sxs-lookup"><span data-stu-id="a82dc-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="a82dc-116">*Радиус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a82dc-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a82dc-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a82dc-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a82dc-118">Радиус сферических источников освещения.</span><span class="sxs-lookup"><span data-stu-id="a82dc-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="a82dc-119">*Ринтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a82dc-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a82dc-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a82dc-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a82dc-121">Красная интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="a82dc-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="a82dc-122">*Гинтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a82dc-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a82dc-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a82dc-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a82dc-124">Зеленая интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="a82dc-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="a82dc-125">*Бинтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a82dc-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a82dc-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a82dc-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a82dc-127">Синяя интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="a82dc-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="a82dc-128">*Праут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a82dc-128">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a82dc-129">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a82dc-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a82dc-130">Указатель на выходной вектор SH для красного компонента.</span><span class="sxs-lookup"><span data-stu-id="a82dc-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="a82dc-131">*пгаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a82dc-131">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a82dc-132">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a82dc-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a82dc-133">Указатель на выходной вектор SH для зеленого компонента.</span><span class="sxs-lookup"><span data-stu-id="a82dc-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="a82dc-134">*пбаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a82dc-134">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a82dc-135">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a82dc-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a82dc-136">Указатель на выходной вектор SH для синего компонента.</span><span class="sxs-lookup"><span data-stu-id="a82dc-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a82dc-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a82dc-137">Return value</span></span>

<span data-ttu-id="a82dc-138">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a82dc-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a82dc-139">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a82dc-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a82dc-140">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="a82dc-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a82dc-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a82dc-141">Remarks</span></span>

<span data-ttu-id="a82dc-142">Оценивает сферическую индикацию и возвращает Спектрал данные SH.</span><span class="sxs-lookup"><span data-stu-id="a82dc-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="a82dc-143">Не существует нормализации интенсивности света, подобного для [направленного освещения](light-types.md), поэтому при указании интенситиес необходимо учитывать осторожность.</span><span class="sxs-lookup"><span data-stu-id="a82dc-143">There is no normalization of the intensity of the light like there is for [directional lights](light-types.md), so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="a82dc-144">Будет выполнено вычисление трех примеров Спектрал. *Праут* будет возвращен, тогда как *пгаут* и *пбаут* могут быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="a82dc-144">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="a82dc-145">В сфере с радиусом единицы, как показано на следующем рисунке, направление может быть задано просто с помощью тета, угла относительно оси z в [правильном направлении](coordinate-systems.md), а значение фи — от z.</span><span class="sxs-lookup"><span data-stu-id="a82dc-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Иллюстрация сферы с радиусом единицы](images/spherical-coordinates.png)

<span data-ttu-id="a82dc-147">В следующих уравнениях показана связь между координатами декартовы (x, y, z) и сферами (тета, фи) в единичной сфере.</span><span class="sxs-lookup"><span data-stu-id="a82dc-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="a82dc-148">Угол тета зависит от диапазона от 0 до 2 Пи, а значение фи отличается от 0 до PI.</span><span class="sxs-lookup"><span data-stu-id="a82dc-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![формулы связи между декартовы и сферыми координатами](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="a82dc-150">Требования</span><span class="sxs-lookup"><span data-stu-id="a82dc-150">Requirements</span></span>



| <span data-ttu-id="a82dc-151">Требование</span><span class="sxs-lookup"><span data-stu-id="a82dc-151">Requirement</span></span> | <span data-ttu-id="a82dc-152">Значение</span><span class="sxs-lookup"><span data-stu-id="a82dc-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a82dc-153">Header</span><span class="sxs-lookup"><span data-stu-id="a82dc-153">Header</span></span><br/>  | <dl> <span data-ttu-id="a82dc-154"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a82dc-154"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a82dc-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a82dc-155">Library</span></span><br/> | <dl> <span data-ttu-id="a82dc-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a82dc-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a82dc-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a82dc-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a82dc-158">Математические функции</span><span class="sxs-lookup"><span data-stu-id="a82dc-158">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a82dc-159">Предварительно вычисленный перенос Радианце (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a82dc-159">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
