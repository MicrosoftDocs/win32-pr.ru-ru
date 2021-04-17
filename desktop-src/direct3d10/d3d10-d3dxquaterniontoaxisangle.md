---
description: Выполняет вычисление оси и угла поворота кватерниона.
ms.assetid: 1e81b88b-071d-46f1-b640-c70d063a14d1
title: Функция D3DXQuaternionToAxisAngle (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0fabba670bbfe83a3032e5a6fa78f5db16c89b3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703907"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx10mathh"></a><span data-ttu-id="688c1-103">Функция D3DXQuaternionToAxisAngle (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="688c1-103">D3DXQuaternionToAxisAngle function (D3DX10Math.h)</span></span>

<span data-ttu-id="688c1-104">Выполняет вычисление оси и угла поворота кватерниона.</span><span class="sxs-lookup"><span data-stu-id="688c1-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="688c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="688c1-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="688c1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="688c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="688c1-107">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="688c1-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="688c1-108">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="688c1-108">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="688c1-109">Указатель на источник [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="688c1-109">Pointer to the source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

</dd> <dt>

<span data-ttu-id="688c1-110">*паксис* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="688c1-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="688c1-111">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="688c1-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="688c1-112">Эта функция возвращает указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , определяющий ось поворота кватерниона.</span><span class="sxs-lookup"><span data-stu-id="688c1-112">This function returns a pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="688c1-113">*пангле* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="688c1-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="688c1-114">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="688c1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="688c1-115">Эта функция возвращает указатель на значение FLOAT, идентифицирующее угол поворота кватерниона в радианах.</span><span class="sxs-lookup"><span data-stu-id="688c1-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="688c1-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="688c1-116">Return value</span></span>

<span data-ttu-id="688c1-117">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="688c1-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="688c1-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="688c1-118">Remarks</span></span>

<span data-ttu-id="688c1-119">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="688c1-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="688c1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="688c1-120">Requirements</span></span>



| <span data-ttu-id="688c1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="688c1-121">Requirement</span></span> | <span data-ttu-id="688c1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="688c1-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="688c1-123">Header</span><span class="sxs-lookup"><span data-stu-id="688c1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="688c1-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="688c1-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="688c1-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="688c1-125">Library</span></span><br/> | <dl> <span data-ttu-id="688c1-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="688c1-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="688c1-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="688c1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="688c1-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="688c1-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
