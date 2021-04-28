---
description: Функция D3DXMatrixDecompose (D3dx9math. h) — разделяет общую матрицу трехмерного преобразования на скалярные, ротации и преобразованные компоненты.
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
ms.openlocfilehash: aaaa1059c4ffeafa453694d9c348656c856decaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098192"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a><span data-ttu-id="5df38-103">Функция D3DXMatrixDecompose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5df38-103">D3DXMatrixDecompose function (D3dx9math.h)</span></span>

<span data-ttu-id="5df38-104">Разделяет общую матрицу трехмерного преобразования на скалярные, ротации и преобразованные компоненты.</span><span class="sxs-lookup"><span data-stu-id="5df38-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="5df38-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5df38-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="5df38-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5df38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5df38-107">*паутскале* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="5df38-107">*pOutScale* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5df38-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5df38-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5df38-109">Указатель на выходную [**D3DXVECTOR3**](d3dxvector3.md) , содержащую коэффициенты масштабирования, применяемые вдоль осей x, y и z.</span><span class="sxs-lookup"><span data-stu-id="5df38-109">Pointer to the output [**D3DXVECTOR3**](d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="5df38-110">*паутротатион* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="5df38-110">*pOutRotation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5df38-111">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="5df38-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5df38-112">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , описывающую поворот.</span><span class="sxs-lookup"><span data-stu-id="5df38-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="5df38-113">*пауттранслатион* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="5df38-113">*pOutTranslation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5df38-114">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5df38-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5df38-115">Указатель на вектор [**D3DXVECTOR3**](d3dxvector3.md) , описывающий преобразование.</span><span class="sxs-lookup"><span data-stu-id="5df38-115">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="5df38-116">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5df38-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5df38-117">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5df38-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5df38-118">Указатель на входную матрицу [**D3DXMATRIX**](d3dxmatrix.md) для разложения.</span><span class="sxs-lookup"><span data-stu-id="5df38-118">Pointer to an input [**D3DXMATRIX**](d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5df38-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5df38-119">Return value</span></span>

<span data-ttu-id="5df38-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5df38-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5df38-121">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5df38-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5df38-122">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="5df38-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5df38-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5df38-123">Requirements</span></span>



| <span data-ttu-id="5df38-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5df38-124">Requirement</span></span> | <span data-ttu-id="5df38-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5df38-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5df38-126">Header</span><span class="sxs-lookup"><span data-stu-id="5df38-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5df38-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5df38-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5df38-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5df38-128">Library</span></span><br/> | <dl> <span data-ttu-id="5df38-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5df38-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5df38-130">См. также</span><span class="sxs-lookup"><span data-stu-id="5df38-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5df38-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="5df38-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




