---
description: Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.
ms.assetid: c69f5ea7-5d14-4187-9405-1ceff8230185
title: 'Метод ID3DXMATRIXStack:: Ротатэйавпитчролллокал (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRollLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cffacf4129a711dece35fd581f6cfc9bc12c2f99
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354330"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx9mathh"></a><span data-ttu-id="5623f-103">Метод ID3DXMATRIXStack:: Ротатэйавпитчролллокал (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5623f-103">ID3DXMATRIXStack::RotateYawPitchRollLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="5623f-104">Поворачивает (относительно локального пространства координат объекта) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="5623f-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="5623f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5623f-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRollLocal(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="5623f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5623f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5623f-107">*Значения нутации* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5623f-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5623f-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5623f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5623f-109">Значения нутации вокруг оси y в радианах.</span><span class="sxs-lookup"><span data-stu-id="5623f-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="5623f-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5623f-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5623f-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5623f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5623f-112">Шаг вокруг оси x в радианах.</span><span class="sxs-lookup"><span data-stu-id="5623f-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="5623f-113">*Рулон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5623f-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5623f-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5623f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5623f-115">Поворот вокруг оси z в радианах.</span><span class="sxs-lookup"><span data-stu-id="5623f-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5623f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5623f-116">Return value</span></span>

<span data-ttu-id="5623f-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5623f-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5623f-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5623f-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5623f-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5623f-119">Remarks</span></span>

<span data-ttu-id="5623f-120">Этот метод добавляет поворот в стек матриц с помощью вычисленной матрицы вращения, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="5623f-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="5623f-121">Так как поворот влево умножается на стек матрицы, поворот происходит относительно локального пространства координат объекта.</span><span class="sxs-lookup"><span data-stu-id="5623f-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="5623f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5623f-122">Requirements</span></span>



| <span data-ttu-id="5623f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="5623f-123">Requirement</span></span> | <span data-ttu-id="5623f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="5623f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5623f-125">Header</span><span class="sxs-lookup"><span data-stu-id="5623f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5623f-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5623f-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5623f-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5623f-127">Library</span></span><br/> | <dl> <span data-ttu-id="5623f-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5623f-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5623f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5623f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5623f-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="5623f-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5623f-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="5623f-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="5623f-132">**ID3DXMATRIXStack:: Ротатеаксис**</span><span class="sxs-lookup"><span data-stu-id="5623f-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="5623f-133">**ID3DXMATRIXStack:: Ротатеаксислокал**</span><span class="sxs-lookup"><span data-stu-id="5623f-133">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="5623f-134">**ID3DXMATRIXStack:: Ротатэйавпитчролл**</span><span class="sxs-lookup"><span data-stu-id="5623f-134">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> </dl>

 

 
