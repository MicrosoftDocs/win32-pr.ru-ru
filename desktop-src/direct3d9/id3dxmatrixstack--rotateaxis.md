---
description: 'Метод ID3DXMATRIXStack:: Ротатеаксис (D3dx9math. h) — поворачивает (относительно мирового пространства координат) вокруг произвольной оси.'
ms.assetid: b7ae5195-a2af-429f-9a0d-51cd7e955362
title: 'Метод ID3DXMATRIXStack:: Ротатеаксис (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ea62b65bca73eb3fe7b2cd962e1afd9b35d53bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093492"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx9mathh"></a><span data-ttu-id="ce5c6-103">Метод ID3DXMATRIXStack:: Ротатеаксис (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ce5c6-103">ID3DXMATRIXStack::RotateAxis method (D3dx9math.h)</span></span>

<span data-ttu-id="ce5c6-104">Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="ce5c6-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce5c6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce5c6-105">Syntax</span></span>


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="ce5c6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce5c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce5c6-107">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce5c6-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5c6-108">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ce5c6-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ce5c6-109">Указатель на произвольную ось поворота.</span><span class="sxs-lookup"><span data-stu-id="ce5c6-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="ce5c6-110">См. [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="ce5c6-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce5c6-111">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ce5c6-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce5c6-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce5c6-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce5c6-113">Угол поворота для произвольной оси в радианах.</span><span class="sxs-lookup"><span data-stu-id="ce5c6-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="ce5c6-114">Углы измеряются против часовой стрелки при просмотре произвольной оси в направлении к источнику.</span><span class="sxs-lookup"><span data-stu-id="ce5c6-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce5c6-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce5c6-115">Return value</span></span>

<span data-ttu-id="ce5c6-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce5c6-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce5c6-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ce5c6-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ce5c6-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="ce5c6-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce5c6-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="ce5c6-119">Remarks</span></span>

<span data-ttu-id="ce5c6-120">Этот метод добавляет поворот в стек матриц с помощью вычисленной матрицы вращения, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="ce5c6-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="ce5c6-121">Так как поворот разворачивается вправо до стека матрицы, вращение происходит относительно пространства координат мира.</span><span class="sxs-lookup"><span data-stu-id="ce5c6-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce5c6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ce5c6-122">Requirements</span></span>



| <span data-ttu-id="ce5c6-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ce5c6-123">Requirement</span></span> | <span data-ttu-id="ce5c6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ce5c6-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce5c6-125">Header</span><span class="sxs-lookup"><span data-stu-id="ce5c6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ce5c6-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce5c6-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ce5c6-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ce5c6-127">Library</span></span><br/> | <dl> <span data-ttu-id="ce5c6-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce5c6-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ce5c6-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ce5c6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce5c6-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="ce5c6-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="ce5c6-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="ce5c6-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="ce5c6-132">**ID3DXMATRIXStack:: Ротатеаксислокал**</span><span class="sxs-lookup"><span data-stu-id="ce5c6-132">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="ce5c6-133">**ID3DXMATRIXStack:: Ротатэйавпитчролл**</span><span class="sxs-lookup"><span data-stu-id="ce5c6-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="ce5c6-134">**ID3DXMATRIXStack:: Ротатэйавпитчролллокал**</span><span class="sxs-lookup"><span data-stu-id="ce5c6-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
