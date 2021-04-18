---
description: Разделяет общую матрицу трехмерного преобразования на скалярные, ротации и преобразованные компоненты.
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: Функция D3DXMatrixDecompose (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92f120f1c3637216d77a5298b5de219f5605d571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694250"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a><span data-ttu-id="72cfe-103">Функция D3DXMatrixDecompose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="72cfe-103">D3DXMatrixDecompose function (D3dx9math.h)</span></span>

<span data-ttu-id="72cfe-104">Разделяет общую матрицу трехмерного преобразования на скалярные, ротации и преобразованные компоненты.</span><span class="sxs-lookup"><span data-stu-id="72cfe-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="72cfe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72cfe-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="72cfe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="72cfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72cfe-107">*паутскале* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="72cfe-107">*pOutScale* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="72cfe-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="72cfe-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="72cfe-109">Указатель на выходную [**D3DXVECTOR3**](d3dxvector3.md) , содержащую коэффициенты масштабирования, применяемые вдоль осей x, y и z.</span><span class="sxs-lookup"><span data-stu-id="72cfe-109">Pointer to the output [**D3DXVECTOR3**](d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="72cfe-110">*паутротатион* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="72cfe-110">*pOutRotation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="72cfe-111">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="72cfe-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="72cfe-112">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , описывающую поворот.</span><span class="sxs-lookup"><span data-stu-id="72cfe-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="72cfe-113">*пауттранслатион* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="72cfe-113">*pOutTranslation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="72cfe-114">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="72cfe-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="72cfe-115">Указатель на вектор [**D3DXVECTOR3**](d3dxvector3.md) , описывающий преобразование.</span><span class="sxs-lookup"><span data-stu-id="72cfe-115">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="72cfe-116">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="72cfe-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72cfe-117">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="72cfe-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="72cfe-118">Указатель на входную матрицу [**D3DXMATRIX**](d3dxmatrix.md) для разложения.</span><span class="sxs-lookup"><span data-stu-id="72cfe-118">Pointer to an input [**D3DXMATRIX**](d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72cfe-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72cfe-119">Return value</span></span>

<span data-ttu-id="72cfe-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="72cfe-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="72cfe-121">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="72cfe-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="72cfe-122">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="72cfe-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="72cfe-123">Требования</span><span class="sxs-lookup"><span data-stu-id="72cfe-123">Requirements</span></span>



| <span data-ttu-id="72cfe-124">Требование</span><span class="sxs-lookup"><span data-stu-id="72cfe-124">Requirement</span></span> | <span data-ttu-id="72cfe-125">Значение</span><span class="sxs-lookup"><span data-stu-id="72cfe-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72cfe-126">Header</span><span class="sxs-lookup"><span data-stu-id="72cfe-126">Header</span></span><br/>  | <dl> <span data-ttu-id="72cfe-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="72cfe-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="72cfe-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="72cfe-128">Library</span></span><br/> | <dl> <span data-ttu-id="72cfe-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72cfe-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="72cfe-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72cfe-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72cfe-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="72cfe-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




