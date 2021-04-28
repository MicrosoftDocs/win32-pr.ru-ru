---
description: Функция D3DXMatrixDecompose (D3DX10Math. h) — разделяет общую матрицу трехмерного преобразования на скалярные, ротации и преобразованные компоненты.
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: Функция D3DXMatrixDecompose (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc87de99d72283c20f25b15ea8d0e5864e2550d9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113212"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a><span data-ttu-id="a104f-103">Функция D3DXMatrixDecompose (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a104f-103">D3DXMatrixDecompose function (D3DX10Math.h)</span></span>

<span data-ttu-id="a104f-104">Разделяет общую матрицу трехмерного преобразования на скалярные, ротации и преобразованные компоненты.</span><span class="sxs-lookup"><span data-stu-id="a104f-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="a104f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a104f-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="a104f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a104f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a104f-107">*паутскале* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a104f-107">*pOutScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a104f-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a104f-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a104f-109">Указатель на выходную [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , содержащую коэффициенты масштабирования, применяемые вдоль осей x, y и z.</span><span class="sxs-lookup"><span data-stu-id="a104f-109">Pointer to the output [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="a104f-110">*паутротатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a104f-110">*pOutRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a104f-111">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="a104f-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a104f-112">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , описывающий поворот.</span><span class="sxs-lookup"><span data-stu-id="a104f-112">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="a104f-113">*пауттранслатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a104f-113">*pOutTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a104f-114">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a104f-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a104f-115">Указатель на вектор D3DXVECTOR3, описывающий преобразование.</span><span class="sxs-lookup"><span data-stu-id="a104f-115">Pointer to the D3DXVECTOR3 vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="a104f-116">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a104f-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a104f-117">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a104f-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a104f-118">Указатель на входную матрицу [**D3DXMATRIX**](d3d10-d3dxmatrix.md) для разложения.</span><span class="sxs-lookup"><span data-stu-id="a104f-118">Pointer to an input [**D3DXMATRIX**](d3d10-d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a104f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a104f-119">Return value</span></span>

<span data-ttu-id="a104f-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a104f-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a104f-121">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a104f-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a104f-122">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="a104f-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a104f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a104f-123">Requirements</span></span>



| <span data-ttu-id="a104f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a104f-124">Requirement</span></span> | <span data-ttu-id="a104f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a104f-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a104f-126">Header</span><span class="sxs-lookup"><span data-stu-id="a104f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a104f-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a104f-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a104f-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a104f-128">Library</span></span><br/> | <dl> <span data-ttu-id="a104f-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a104f-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a104f-130">См. также</span><span class="sxs-lookup"><span data-stu-id="a104f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a104f-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="a104f-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
