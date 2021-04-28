---
description: 'Метод ID3DXMATRIXStack:: Ротатеаксислокал (D3dx9math. h) — поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.'
ms.assetid: c7ef11e9-f4c4-4801-8f25-190066baeb52
title: 'Метод ID3DXMATRIXStack:: Ротатеаксислокал (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0bfcfd7301f90dcf49b03e7bbb3fd7e3b0de6c3e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093472"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx9mathh"></a><span data-ttu-id="c388f-103">Метод ID3DXMATRIXStack:: Ротатеаксислокал (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c388f-103">ID3DXMATRIXStack::RotateAxisLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="c388f-104">Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="c388f-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="c388f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c388f-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="c388f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c388f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c388f-107">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c388f-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c388f-108">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c388f-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c388f-109">Указатель на произвольную ось поворота.</span><span class="sxs-lookup"><span data-stu-id="c388f-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="c388f-110">См. [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="c388f-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="c388f-111">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c388f-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c388f-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c388f-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c388f-113">Угол поворота для произвольной оси в радианах.</span><span class="sxs-lookup"><span data-stu-id="c388f-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="c388f-114">Углы измеряются против часовой стрелки при просмотре произвольной оси в направлении к источнику.</span><span class="sxs-lookup"><span data-stu-id="c388f-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c388f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c388f-115">Return value</span></span>

<span data-ttu-id="c388f-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c388f-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c388f-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c388f-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c388f-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="c388f-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c388f-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="c388f-119">Remarks</span></span>

<span data-ttu-id="c388f-120">Этот метод добавляет поворот в стек матриц с помощью вычисленной матрицы вращения, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="c388f-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="c388f-121">Так как поворот влево умножается на стек матрицы, поворот происходит относительно локального пространства координат объекта.</span><span class="sxs-lookup"><span data-stu-id="c388f-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="c388f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c388f-122">Requirements</span></span>



| <span data-ttu-id="c388f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c388f-123">Requirement</span></span> | <span data-ttu-id="c388f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c388f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c388f-125">Header</span><span class="sxs-lookup"><span data-stu-id="c388f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c388f-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c388f-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c388f-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c388f-127">Library</span></span><br/> | <dl> <span data-ttu-id="c388f-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c388f-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c388f-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c388f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c388f-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="c388f-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="c388f-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="c388f-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="c388f-132">**ID3DXMATRIXStack:: Ротатеаксис**</span><span class="sxs-lookup"><span data-stu-id="c388f-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="c388f-133">**ID3DXMATRIXStack:: Ротатэйавпитчролл**</span><span class="sxs-lookup"><span data-stu-id="c388f-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="c388f-134">**ID3DXMATRIXStack:: Ротатэйавпитчролллокал**</span><span class="sxs-lookup"><span data-stu-id="c388f-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
