---
description: Разделяет общую матрицу трехмерного преобразования на скалярные, ротации и преобразованные компоненты.
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
ms.openlocfilehash: 507c8f177db0f71b3d333a8343e4166e649f424a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273929"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a><span data-ttu-id="fad76-103">Функция D3DXMatrixDecompose (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="fad76-103">D3DXMatrixDecompose function (D3DX10Math.h)</span></span>

<span data-ttu-id="fad76-104">Разделяет общую матрицу трехмерного преобразования на скалярные, ротации и преобразованные компоненты.</span><span class="sxs-lookup"><span data-stu-id="fad76-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad76-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fad76-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="fad76-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fad76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fad76-107">*паутскале* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fad76-107">*pOutScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fad76-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fad76-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fad76-109">Указатель на выходную [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , содержащую коэффициенты масштабирования, применяемые вдоль осей x, y и z.</span><span class="sxs-lookup"><span data-stu-id="fad76-109">Pointer to the output [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="fad76-110">*паутротатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fad76-110">*pOutRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fad76-111">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fad76-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fad76-112">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , описывающий поворот.</span><span class="sxs-lookup"><span data-stu-id="fad76-112">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="fad76-113">*пауттранслатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fad76-113">*pOutTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fad76-114">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fad76-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="fad76-115">Указатель на вектор D3DXVECTOR3, описывающий преобразование.</span><span class="sxs-lookup"><span data-stu-id="fad76-115">Pointer to the D3DXVECTOR3 vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="fad76-116">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fad76-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fad76-117">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fad76-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fad76-118">Указатель на входную матрицу [**D3DXMATRIX**](d3d10-d3dxmatrix.md) для разложения.</span><span class="sxs-lookup"><span data-stu-id="fad76-118">Pointer to an input [**D3DXMATRIX**](d3d10-d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fad76-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fad76-119">Return value</span></span>

<span data-ttu-id="fad76-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fad76-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fad76-121">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fad76-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fad76-122">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="fad76-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fad76-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fad76-123">Requirements</span></span>



| <span data-ttu-id="fad76-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fad76-124">Requirement</span></span> | <span data-ttu-id="fad76-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fad76-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fad76-126">Header</span><span class="sxs-lookup"><span data-stu-id="fad76-126">Header</span></span><br/>  | <dl> <span data-ttu-id="fad76-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fad76-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="fad76-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fad76-128">Library</span></span><br/> | <dl> <span data-ttu-id="fad76-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fad76-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fad76-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fad76-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad76-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="fad76-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
