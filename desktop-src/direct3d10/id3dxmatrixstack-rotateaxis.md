---
description: 'Метод ID3DXMATRIXStack:: Ротатеаксис (D3DX10. h) — поворачивает (относительно мирового пространства координат) вокруг произвольной оси.'
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
ms.openlocfilehash: 0a2e52eed1c1957de9a0fcfed4ba3d3d05f89cb9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107916"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx10h"></a><span data-ttu-id="b2769-103">Метод ID3DXMATRIXStack:: Ротатеаксис (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="b2769-103">ID3DXMATRIXStack::RotateAxis method (D3DX10.h)</span></span>

<span data-ttu-id="b2769-104">Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="b2769-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2769-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2769-105">Syntax</span></span>


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="b2769-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2769-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2769-107">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2769-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2769-108">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b2769-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b2769-109">Указатель на произвольную ось поворота.</span><span class="sxs-lookup"><span data-stu-id="b2769-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="b2769-110">См. [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="b2769-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2769-111">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2769-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2769-112">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2769-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2769-113">Угол поворота для произвольной оси в радианах.</span><span class="sxs-lookup"><span data-stu-id="b2769-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="b2769-114">Углы измеряются против часовой стрелки при просмотре произвольной оси в направлении к источнику.</span><span class="sxs-lookup"><span data-stu-id="b2769-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2769-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2769-115">Return value</span></span>

<span data-ttu-id="b2769-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2769-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2769-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b2769-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b2769-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="b2769-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2769-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="b2769-119">Remarks</span></span>

<span data-ttu-id="b2769-120">Этот метод добавляет поворот в стек матриц с помощью вычисленной матрицы вращения, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="b2769-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="b2769-121">Так как поворот разворачивается вправо до стека матрицы, вращение происходит относительно пространства координат мира.</span><span class="sxs-lookup"><span data-stu-id="b2769-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2769-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b2769-122">Requirements</span></span>



| <span data-ttu-id="b2769-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b2769-123">Requirement</span></span> | <span data-ttu-id="b2769-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b2769-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2769-125">Header</span><span class="sxs-lookup"><span data-stu-id="b2769-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b2769-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2769-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2769-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b2769-127">Library</span></span><br/> | <dl> <span data-ttu-id="b2769-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2769-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2769-129">См. также</span><span class="sxs-lookup"><span data-stu-id="b2769-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2769-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="b2769-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="b2769-131">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="b2769-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
