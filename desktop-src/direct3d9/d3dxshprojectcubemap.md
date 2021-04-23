---
description: Проецирует функцию, представленную на схеме Куба, в сферические гармонические колебания (SH).
ms.assetid: da5a3195-801e-4f1c-b52c-9eafc6e2e7b4
title: Функция D3DXSHProjectCubeMap (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHProjectCubeMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0e3e45b42907c47d8c7f1b9e5294738b8997cd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713898"
---
# <a name="d3dxshprojectcubemap-function"></a><span data-ttu-id="bf647-103">Функция D3DXSHProjectCubeMap</span><span class="sxs-lookup"><span data-stu-id="bf647-103">D3DXSHProjectCubeMap function</span></span>

<span data-ttu-id="bf647-104">Проецирует функцию, представленную на схеме Куба, в сферические гармонические колебания (SH).</span><span class="sxs-lookup"><span data-stu-id="bf647-104">Projects a function represented on a cube map into spherical harmonics (SH).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf647-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf647-105">Syntax</span></span>


```C++
HRESULT D3DXSHProjectCubeMap(
  _In_ UINT                   Order,
  _In_ LPDIRECT3DCUBETEXTURE9 pCubeMap,
  _In_ FLOAT                  *pROut,
  _In_ FLOAT                  *pGOut,
  _In_ FLOAT                  *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="bf647-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf647-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf647-107">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf647-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf647-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf647-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf647-109">Порядок вычисления сферического гармонического (SH).</span><span class="sxs-lookup"><span data-stu-id="bf647-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="bf647-110">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="bf647-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="bf647-111">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="bf647-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="bf647-112">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="bf647-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="bf647-113">*пкубемап* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf647-113">*pCubeMap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf647-114">Тип: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="bf647-114">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="bf647-115">Указатель на текстуру исходного куба.</span><span class="sxs-lookup"><span data-stu-id="bf647-115">Pointer to a source cube texture.</span></span> <span data-ttu-id="bf647-116">См. [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9).</span><span class="sxs-lookup"><span data-stu-id="bf647-116">See [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9).</span></span>

</dd> <dt>

<span data-ttu-id="bf647-117">*Праут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf647-117">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf647-118">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf647-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bf647-119">Указатель на выходной вектор SH для красного компонента.</span><span class="sxs-lookup"><span data-stu-id="bf647-119">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="bf647-120">*пгаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf647-120">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf647-121">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf647-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bf647-122">Указатель на выходной вектор SH для зеленого компонента.</span><span class="sxs-lookup"><span data-stu-id="bf647-122">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="bf647-123">*пбаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf647-123">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf647-124">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf647-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bf647-125">Указатель на выходной вектор SH для синего компонента.</span><span class="sxs-lookup"><span data-stu-id="bf647-125">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf647-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf647-126">Return value</span></span>

<span data-ttu-id="bf647-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bf647-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bf647-128">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bf647-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bf647-129">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="bf647-129">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf647-130">Требования</span><span class="sxs-lookup"><span data-stu-id="bf647-130">Requirements</span></span>



| <span data-ttu-id="bf647-131">Требование</span><span class="sxs-lookup"><span data-stu-id="bf647-131">Requirement</span></span> | <span data-ttu-id="bf647-132">Значение</span><span class="sxs-lookup"><span data-stu-id="bf647-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf647-133">Header</span><span class="sxs-lookup"><span data-stu-id="bf647-133">Header</span></span><br/>  | <dl> <span data-ttu-id="bf647-134"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf647-134"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bf647-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf647-135">Library</span></span><br/> | <dl> <span data-ttu-id="bf647-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf647-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bf647-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf647-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf647-138">Математические функции</span><span class="sxs-lookup"><span data-stu-id="bf647-138">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="bf647-139">Предварительно вычисленный перенос Радианце (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bf647-139">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
