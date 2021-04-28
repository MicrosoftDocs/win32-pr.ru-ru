---
description: Функция D3DXQuaternionToAxisAngle (D3dx9math. h) — вычисление оси и угла поворота кватерниона.
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: Функция D3DXQuaternionToAxisAngle (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8613a9d14c5e33b0f9f4e719a02ac9a6d70d1119
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117982"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a><span data-ttu-id="fd8cf-103">Функция D3DXQuaternionToAxisAngle (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fd8cf-103">D3DXQuaternionToAxisAngle function (D3dx9math.h)</span></span>

<span data-ttu-id="fd8cf-104">Выполняет вычисление оси и угла поворота кватерниона.</span><span class="sxs-lookup"><span data-stu-id="fd8cf-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd8cf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd8cf-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="fd8cf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd8cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd8cf-107">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd8cf-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd8cf-108">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd8cf-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fd8cf-109">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="fd8cf-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fd8cf-110">*паксис* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="fd8cf-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd8cf-111">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd8cf-111">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fd8cf-112">Эта функция возвращает указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая идентифицирует ось вращения кватернион.</span><span class="sxs-lookup"><span data-stu-id="fd8cf-112">This function returns a pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="fd8cf-113">*пангле* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="fd8cf-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd8cf-114">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd8cf-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fd8cf-115">Эта функция возвращает указатель на значение FLOAT, идентифицирующее угол поворота кватерниона в радианах.</span><span class="sxs-lookup"><span data-stu-id="fd8cf-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd8cf-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd8cf-116">Return value</span></span>

<span data-ttu-id="fd8cf-117">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="fd8cf-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd8cf-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="fd8cf-118">Remarks</span></span>

<span data-ttu-id="fd8cf-119">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="fd8cf-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd8cf-120">Требования</span><span class="sxs-lookup"><span data-stu-id="fd8cf-120">Requirements</span></span>



| <span data-ttu-id="fd8cf-121">Требование</span><span class="sxs-lookup"><span data-stu-id="fd8cf-121">Requirement</span></span> | <span data-ttu-id="fd8cf-122">Значение</span><span class="sxs-lookup"><span data-stu-id="fd8cf-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd8cf-123">Header</span><span class="sxs-lookup"><span data-stu-id="fd8cf-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fd8cf-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd8cf-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fd8cf-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fd8cf-125">Library</span></span><br/> | <dl> <span data-ttu-id="fd8cf-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd8cf-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fd8cf-127">См. также</span><span class="sxs-lookup"><span data-stu-id="fd8cf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd8cf-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="fd8cf-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
