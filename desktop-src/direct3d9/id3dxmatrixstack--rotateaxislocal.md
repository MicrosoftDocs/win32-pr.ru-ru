---
description: Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.
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
ms.openlocfilehash: 8488f6314eb926495baa2e42df9ea01616131507
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713550"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx9mathh"></a><span data-ttu-id="8fcc8-103">Метод ID3DXMATRIXStack:: Ротатеаксислокал (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8fcc8-103">ID3DXMATRIXStack::RotateAxisLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="8fcc8-104">Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="8fcc8-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fcc8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fcc8-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="8fcc8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fcc8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fcc8-107">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8fcc8-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fcc8-108">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8fcc8-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8fcc8-109">Указатель на произвольную ось поворота.</span><span class="sxs-lookup"><span data-stu-id="8fcc8-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="8fcc8-110">См. [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="8fcc8-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fcc8-111">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8fcc8-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fcc8-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8fcc8-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8fcc8-113">Угол поворота для произвольной оси в радианах.</span><span class="sxs-lookup"><span data-stu-id="8fcc8-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="8fcc8-114">Углы измеряются против часовой стрелки при просмотре произвольной оси в направлении к источнику.</span><span class="sxs-lookup"><span data-stu-id="8fcc8-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fcc8-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fcc8-115">Return value</span></span>

<span data-ttu-id="8fcc8-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8fcc8-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8fcc8-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8fcc8-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8fcc8-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="8fcc8-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fcc8-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8fcc8-119">Remarks</span></span>

<span data-ttu-id="8fcc8-120">Этот метод добавляет поворот в стек матриц с помощью вычисленной матрицы вращения, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="8fcc8-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="8fcc8-121">Так как поворот влево умножается на стек матрицы, поворот происходит относительно локального пространства координат объекта.</span><span class="sxs-lookup"><span data-stu-id="8fcc8-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fcc8-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8fcc8-122">Requirements</span></span>



| <span data-ttu-id="8fcc8-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8fcc8-123">Requirement</span></span> | <span data-ttu-id="8fcc8-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8fcc8-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fcc8-125">Header</span><span class="sxs-lookup"><span data-stu-id="8fcc8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8fcc8-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fcc8-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8fcc8-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8fcc8-127">Library</span></span><br/> | <dl> <span data-ttu-id="8fcc8-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fcc8-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8fcc8-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fcc8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fcc8-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="8fcc8-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="8fcc8-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="8fcc8-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="8fcc8-132">**ID3DXMATRIXStack:: Ротатеаксис**</span><span class="sxs-lookup"><span data-stu-id="8fcc8-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="8fcc8-133">**ID3DXMATRIXStack:: Ротатэйавпитчролл**</span><span class="sxs-lookup"><span data-stu-id="8fcc8-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="8fcc8-134">**ID3DXMATRIXStack:: Ротатэйавпитчролллокал**</span><span class="sxs-lookup"><span data-stu-id="8fcc8-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
