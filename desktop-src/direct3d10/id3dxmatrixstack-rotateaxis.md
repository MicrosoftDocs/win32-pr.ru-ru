---
description: Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.
ms.assetid: 7c842bf6-2d13-422e-8136-0506a76ce9fe
title: 'Метод ID3DXMATRIXStack:: Ротатеаксис (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: badd26d61fa6580b0193039e29a8fceedabe2d3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356000"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx10h"></a><span data-ttu-id="74916-103">Метод ID3DXMATRIXStack:: Ротатеаксис (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="74916-103">ID3DXMATRIXStack::RotateAxis method (D3DX10.h)</span></span>

<span data-ttu-id="74916-104">Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="74916-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="74916-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74916-105">Syntax</span></span>


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="74916-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="74916-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74916-107">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74916-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74916-108">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="74916-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="74916-109">Указатель на произвольную ось поворота.</span><span class="sxs-lookup"><span data-stu-id="74916-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="74916-110">См. [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="74916-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="74916-111">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74916-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74916-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74916-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74916-113">Угол поворота для произвольной оси в радианах.</span><span class="sxs-lookup"><span data-stu-id="74916-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="74916-114">Углы измеряются против часовой стрелки при просмотре произвольной оси в направлении к источнику.</span><span class="sxs-lookup"><span data-stu-id="74916-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74916-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74916-115">Return value</span></span>

<span data-ttu-id="74916-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74916-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74916-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="74916-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="74916-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="74916-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="74916-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74916-119">Remarks</span></span>

<span data-ttu-id="74916-120">Этот метод добавляет поворот в стек матриц с помощью вычисленной матрицы вращения, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="74916-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="74916-121">Так как поворот разворачивается вправо до стека матрицы, вращение происходит относительно пространства координат мира.</span><span class="sxs-lookup"><span data-stu-id="74916-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="74916-122">Требования</span><span class="sxs-lookup"><span data-stu-id="74916-122">Requirements</span></span>



| <span data-ttu-id="74916-123">Требование</span><span class="sxs-lookup"><span data-stu-id="74916-123">Requirement</span></span> | <span data-ttu-id="74916-124">Значение</span><span class="sxs-lookup"><span data-stu-id="74916-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74916-125">Header</span><span class="sxs-lookup"><span data-stu-id="74916-125">Header</span></span><br/>  | <dl> <span data-ttu-id="74916-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="74916-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="74916-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="74916-127">Library</span></span><br/> | <dl> <span data-ttu-id="74916-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74916-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74916-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74916-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74916-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="74916-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="74916-131">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="74916-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
