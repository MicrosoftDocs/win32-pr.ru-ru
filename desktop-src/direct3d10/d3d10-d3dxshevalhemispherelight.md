---
description: Вычисляет освещение, которое является линейной интерполяцией между двумя цветами в сфере.
ms.assetid: 7523ff42-c81d-4857-a50d-7efa213214b8
title: Функция D3DXSHEvalHemisphereLight (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalHemisphereLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c6ff3359ce0629eec472e4da24a31c24196c7f15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355323"
---
# <a name="d3dxshevalhemispherelight-function-d3dx10h"></a><span data-ttu-id="21e00-103">Функция D3DXSHEvalHemisphereLight (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="21e00-103">D3DXSHEvalHemisphereLight function (D3DX10.h)</span></span>

<span data-ttu-id="21e00-104">Вычисляет освещение, которое является линейной интерполяцией между двумя цветами в сфере.</span><span class="sxs-lookup"><span data-stu-id="21e00-104">Evaluates a light that is a linear interpolation between two colors over the sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="21e00-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21e00-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalHemisphereLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       D3DXCOLOR   Top,
  _In_       D3DXCOLOR   Bottom,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="21e00-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="21e00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21e00-107">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e00-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e00-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21e00-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21e00-109">Порядок вычисления сферического гармонического (SH).</span><span class="sxs-lookup"><span data-stu-id="21e00-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="21e00-110">Должен находиться в диапазоне от D3DXSH \_ минордер до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="21e00-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="21e00-111">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="21e00-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="21e00-112">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="21e00-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="21e00-113">*пдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e00-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e00-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="21e00-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="21e00-115">Указатель на вектор направления (x, y, z) полушари оси, в котором оцениваются функции-основания SH.</span><span class="sxs-lookup"><span data-stu-id="21e00-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="21e00-116">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="21e00-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="21e00-117">В *Начало* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e00-117">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e00-118">Тип: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="21e00-118">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="21e00-119">Голубой цвет.</span><span class="sxs-lookup"><span data-stu-id="21e00-119">The sky color.</span></span>

</dd> <dt>

<span data-ttu-id="21e00-120">По *нижнему краю* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e00-120">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e00-121">Тип: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="21e00-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="21e00-122">Цвет заземления.</span><span class="sxs-lookup"><span data-stu-id="21e00-122">The ground color.</span></span>

</dd> <dt>

<span data-ttu-id="21e00-123">*Праут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e00-123">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e00-124">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="21e00-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="21e00-125">Указатель на выходной вектор SH для красного компонента.</span><span class="sxs-lookup"><span data-stu-id="21e00-125">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="21e00-126">*пгаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e00-126">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e00-127">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="21e00-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="21e00-128">Указатель на выходной вектор SH для зеленого компонента.</span><span class="sxs-lookup"><span data-stu-id="21e00-128">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="21e00-129">*пбаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21e00-129">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e00-130">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="21e00-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="21e00-131">Указатель на выходной вектор SH для синего компонента.</span><span class="sxs-lookup"><span data-stu-id="21e00-131">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21e00-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21e00-132">Return value</span></span>

<span data-ttu-id="21e00-133">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21e00-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21e00-134">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="21e00-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="21e00-135">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="21e00-135">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="21e00-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21e00-136">Remarks</span></span>

<span data-ttu-id="21e00-137">Интерполяция выполняется линейно между двумя точками, а не за поверхностью сферы (т. е. Если ось имеет значение (0, 0, 1), линейная — Z, а не в азимусал углом).</span><span class="sxs-lookup"><span data-stu-id="21e00-137">The interpolation is done linearly between the two points, not over the surface of the sphere (that is, if the axis was (0,0,1) it is linear in Z, not in the azimuthal angle).</span></span> <span data-ttu-id="21e00-138">Результирующая функция сферического освещения нормализована таким образом, что точка на идеально рассеянной поверхности без тени и обычной, направленной в направлении Пдир, приведет к выходу радианце со значением 1 (если верхний цвет был белым и нижний цвет был черным).</span><span class="sxs-lookup"><span data-stu-id="21e00-138">The resulting spherical lighting function is normalized so that a point on a perfectly diffuse surface with no shadowing and a normal pointed in the direction pDir would result in exit radiance with a value of 1 (if the top color was white and the bottom color was black).</span></span> <span data-ttu-id="21e00-139">Это очень простая модель, где Top представляет интенсивность "небесной" и нижней части представляет интенсивность "заземления".</span><span class="sxs-lookup"><span data-stu-id="21e00-139">This is a very simple model where Top represents the intensity of the "sky" and Bottom represents the intensity of the "ground."</span></span>

<span data-ttu-id="21e00-140">В сфере с радиусом единицы, как показано на следующем рисунке, направление может быть задано просто с помощью тета, угла относительно оси z в правильном направлении, а значение фи — от z.</span><span class="sxs-lookup"><span data-stu-id="21e00-140">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![Иллюстрация сферы с радиусом единицы](images/spherical-coordinates.png)

<span data-ttu-id="21e00-142">В следующих уравнениях показана связь между координатами декартовы (x, y, z) и сферами (тета, фи) в единичной сфере.</span><span class="sxs-lookup"><span data-stu-id="21e00-142">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="21e00-143">Угол тета зависит от диапазона от 0 до 2 Пи, а значение фи отличается от 0 до PI.</span><span class="sxs-lookup"><span data-stu-id="21e00-143">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![формулы связи между декартовы и сферыми координатами](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="21e00-145">Требования</span><span class="sxs-lookup"><span data-stu-id="21e00-145">Requirements</span></span>



| <span data-ttu-id="21e00-146">Требование</span><span class="sxs-lookup"><span data-stu-id="21e00-146">Requirement</span></span> | <span data-ttu-id="21e00-147">Значение</span><span class="sxs-lookup"><span data-stu-id="21e00-147">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21e00-148">Header</span><span class="sxs-lookup"><span data-stu-id="21e00-148">Header</span></span><br/>  | <dl> <span data-ttu-id="21e00-149"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="21e00-149"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="21e00-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="21e00-150">Library</span></span><br/> | <dl> <span data-ttu-id="21e00-151"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21e00-151"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21e00-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21e00-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21e00-153">Математические функции</span><span class="sxs-lookup"><span data-stu-id="21e00-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
