---
description: 'Метод ID3DXMATRIXStack:: Ротатеаксислокал (D3DX10. h) — поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.'
ms.assetid: 90837762-9bfe-4065-94b3-1ca61184a78e
title: 'Метод ID3DXMATRIXStack:: Ротатеаксислокал (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxisLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a81a4c4bd9a2f738274f98ce925799b34986fbb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107882"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx10h"></a><span data-ttu-id="7e5db-103">Метод ID3DXMATRIXStack:: Ротатеаксислокал (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="7e5db-103">ID3DXMATRIXStack::RotateAxisLocal method (D3DX10.h)</span></span>

<span data-ttu-id="7e5db-104">Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="7e5db-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e5db-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e5db-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="7e5db-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e5db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e5db-107">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e5db-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e5db-108">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e5db-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7e5db-109">Указатель на произвольную ось поворота.</span><span class="sxs-lookup"><span data-stu-id="7e5db-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="7e5db-110">См. [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="7e5db-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e5db-111">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e5db-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e5db-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e5db-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7e5db-113">Угол поворота для произвольной оси в радианах.</span><span class="sxs-lookup"><span data-stu-id="7e5db-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="7e5db-114">Углы измеряются против часовой стрелки при просмотре произвольной оси в направлении к источнику.</span><span class="sxs-lookup"><span data-stu-id="7e5db-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e5db-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e5db-115">Return value</span></span>

<span data-ttu-id="7e5db-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e5db-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e5db-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7e5db-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7e5db-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="7e5db-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e5db-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="7e5db-119">Remarks</span></span>

<span data-ttu-id="7e5db-120">Этот метод добавляет поворот в стек матриц с помощью вычисленной матрицы вращения, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="7e5db-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="7e5db-121">Так как поворот влево умножается на стек матрицы, поворот происходит относительно локального пространства координат объекта.</span><span class="sxs-lookup"><span data-stu-id="7e5db-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e5db-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7e5db-122">Requirements</span></span>



| <span data-ttu-id="7e5db-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7e5db-123">Requirement</span></span> | <span data-ttu-id="7e5db-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7e5db-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e5db-125">Header</span><span class="sxs-lookup"><span data-stu-id="7e5db-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7e5db-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e5db-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e5db-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7e5db-127">Library</span></span><br/> | <dl> <span data-ttu-id="7e5db-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e5db-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e5db-129">См. также</span><span class="sxs-lookup"><span data-stu-id="7e5db-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e5db-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="7e5db-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="7e5db-131">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="7e5db-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
