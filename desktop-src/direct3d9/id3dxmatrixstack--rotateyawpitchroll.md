---
description: Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.
ms.assetid: 25a7eff4-a575-4ddb-85eb-ef3fa2d6ae3b
title: 'Метод ID3DXMATRIXStack:: Ротатэйавпитчролл (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRoll
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5020cb6ff3af41b9ef32ef77bb71607f6cd5ea6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713548"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx9mathh"></a><span data-ttu-id="a177a-103">Метод ID3DXMATRIXStack:: Ротатэйавпитчролл (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a177a-103">ID3DXMATRIXStack::RotateYawPitchRoll method (D3dx9math.h)</span></span>

<span data-ttu-id="a177a-104">Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="a177a-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="a177a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a177a-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="a177a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a177a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a177a-107">*Значения нутации* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a177a-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a177a-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a177a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a177a-109">Значения нутации вокруг оси y в радианах.</span><span class="sxs-lookup"><span data-stu-id="a177a-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="a177a-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a177a-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a177a-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a177a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a177a-112">Шаг вокруг оси x в радианах.</span><span class="sxs-lookup"><span data-stu-id="a177a-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="a177a-113">*Рулон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a177a-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a177a-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a177a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a177a-115">Поворот вокруг оси z в радианах.</span><span class="sxs-lookup"><span data-stu-id="a177a-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a177a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a177a-116">Return value</span></span>

<span data-ttu-id="a177a-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a177a-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a177a-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a177a-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a177a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a177a-119">Remarks</span></span>

<span data-ttu-id="a177a-120">Этот метод добавляет поворот в стек матриц с помощью вычисленной матрицы вращения, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="a177a-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="a177a-121">Так как поворот разворачивается вправо до стека матрицы, вращение происходит относительно пространства координат мира.</span><span class="sxs-lookup"><span data-stu-id="a177a-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="a177a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a177a-122">Requirements</span></span>



| <span data-ttu-id="a177a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a177a-123">Requirement</span></span> | <span data-ttu-id="a177a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a177a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a177a-125">Header</span><span class="sxs-lookup"><span data-stu-id="a177a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a177a-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a177a-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a177a-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a177a-127">Library</span></span><br/> | <dl> <span data-ttu-id="a177a-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a177a-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a177a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a177a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a177a-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="a177a-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="a177a-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="a177a-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="a177a-132">**ID3DXMATRIXStack:: Ротатеаксис**</span><span class="sxs-lookup"><span data-stu-id="a177a-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="a177a-133">**ID3DXMATRIXStack:: Ротатеаксислокал**</span><span class="sxs-lookup"><span data-stu-id="a177a-133">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="a177a-134">**ID3DXMATRIXStack:: Ротатэйавпитчролллокал**</span><span class="sxs-lookup"><span data-stu-id="a177a-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
