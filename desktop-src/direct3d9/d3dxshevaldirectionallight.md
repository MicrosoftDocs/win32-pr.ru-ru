---
description: Оценивает направленный источник данных и возвращает Спектрал сферические гармонические данные (SH).
ms.assetid: 6e2e9b02-13bb-4cef-ae9d-343fbf64e5d7
title: Функция D3DXSHEvalDirectionalLight (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirectionalLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c78ee4059ed83b97e7ac1f392f857351df48ee7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104560332"
---
# <a name="d3dxshevaldirectionallight-function-d3dx9mathh"></a><span data-ttu-id="072e7-103">Функция D3DXSHEvalDirectionalLight (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="072e7-103">D3DXSHEvalDirectionalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="072e7-104">Оценивает [направленный источник](light-types.md) данных и возвращает Спектрал сферические гармонические данные (SH).</span><span class="sxs-lookup"><span data-stu-id="072e7-104">Evaluates a [directional light](light-types.md) and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="072e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="072e7-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="072e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="072e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="072e7-107">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="072e7-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="072e7-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="072e7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="072e7-109">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="072e7-109">Order of the SH evaluation.</span></span> <span data-ttu-id="072e7-110">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="072e7-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="072e7-111">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="072e7-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="072e7-112">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="072e7-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="072e7-113">*пдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="072e7-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="072e7-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="072e7-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="072e7-115">Указатель на вектор направления (x, y, z) полушари оси, в котором оцениваются функции-основания SH.</span><span class="sxs-lookup"><span data-stu-id="072e7-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="072e7-116">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="072e7-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="072e7-117">*Ринтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="072e7-117">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="072e7-118">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="072e7-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="072e7-119">Красная интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="072e7-119">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="072e7-120">*Гинтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="072e7-120">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="072e7-121">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="072e7-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="072e7-122">Зеленая интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="072e7-122">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="072e7-123">*Бинтенсити* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="072e7-123">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="072e7-124">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="072e7-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="072e7-125">Синяя интенсивность освещения.</span><span class="sxs-lookup"><span data-stu-id="072e7-125">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="072e7-126">*Праут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="072e7-126">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="072e7-127">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="072e7-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="072e7-128">Указатель на выходной вектор SH для красного компонента.</span><span class="sxs-lookup"><span data-stu-id="072e7-128">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="072e7-129">*пгаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="072e7-129">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="072e7-130">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="072e7-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="072e7-131">Необязательный указатель на выходной вектор SH для зеленого компонента.</span><span class="sxs-lookup"><span data-stu-id="072e7-131">Optional pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="072e7-132">*пбаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="072e7-132">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="072e7-133">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="072e7-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="072e7-134">Необязательный указатель на выходной вектор SH для синего компонента.</span><span class="sxs-lookup"><span data-stu-id="072e7-134">Optional pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="072e7-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="072e7-135">Return value</span></span>

<span data-ttu-id="072e7-136">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="072e7-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="072e7-137">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="072e7-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="072e7-138">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="072e7-138">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="072e7-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="072e7-139">Remarks</span></span>

<span data-ttu-id="072e7-140">Выходной вектор вычисляются так, что если коэффициент интенсивности R/G/B равен 1, то результирующий радианце точки непосредственно под освещением рассеянного объекта с албедо, равным 1, будет 1,0.</span><span class="sxs-lookup"><span data-stu-id="072e7-140">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the resulting exit radiance of a point directly under the light on a diffuse object with an albedo of 1 would be 1.0.</span></span> <span data-ttu-id="072e7-141">Будет выполнено вычисление трех примеров Спектрал. *Праут* будет возвращен, тогда как *пгаут* и *пбаут* могут быть возвращены.</span><span class="sxs-lookup"><span data-stu-id="072e7-141">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="072e7-142">В сфере с радиусом единицы, как показано на следующем рисунке, направление может быть задано просто с помощью тета, угла относительно оси z в [правильном направлении](coordinate-systems.md), а значение фи — от z.</span><span class="sxs-lookup"><span data-stu-id="072e7-142">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Иллюстрация сферы с радиусом единицы](images/spherical-coordinates.png)

<span data-ttu-id="072e7-144">В следующих уравнениях показана связь между координатами декартовы (x, y, z) и сферами (тета, фи) в единичной сфере.</span><span class="sxs-lookup"><span data-stu-id="072e7-144">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="072e7-145">Угол тета зависит от диапазона от 0 до 2 Пи, а значение фи отличается от 0 до PI.</span><span class="sxs-lookup"><span data-stu-id="072e7-145">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![формулы связи между декартовы и сферыми координатами](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="072e7-147">Требования</span><span class="sxs-lookup"><span data-stu-id="072e7-147">Requirements</span></span>



| <span data-ttu-id="072e7-148">Требование</span><span class="sxs-lookup"><span data-stu-id="072e7-148">Requirement</span></span> | <span data-ttu-id="072e7-149">Значение</span><span class="sxs-lookup"><span data-stu-id="072e7-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="072e7-150">Header</span><span class="sxs-lookup"><span data-stu-id="072e7-150">Header</span></span><br/>  | <dl> <span data-ttu-id="072e7-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="072e7-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="072e7-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="072e7-152">Library</span></span><br/> | <dl> <span data-ttu-id="072e7-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="072e7-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="072e7-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="072e7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="072e7-155">Математические функции</span><span class="sxs-lookup"><span data-stu-id="072e7-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="072e7-156">Предварительно вычисленный перенос Радианце (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="072e7-156">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
