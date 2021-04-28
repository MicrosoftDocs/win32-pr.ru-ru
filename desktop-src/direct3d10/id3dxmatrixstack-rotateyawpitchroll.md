---
description: 'Метод ID3DXMATRIXStack:: Ротатэйавпитчролл (D3DX10. h) — поворачивает (относительно мирового пространства координат) вокруг произвольной оси.'
ms.assetid: 35e237f6-40f2-4001-adb0-f489d61f64e7
title: 'Метод ID3DXMATRIXStack:: Ротатэйавпитчролл (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8c4f167f769a1ed46404028916477d6784e4a436
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107832"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx10h"></a><span data-ttu-id="db8bb-103">Метод ID3DXMATRIXStack:: Ротатэйавпитчролл (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="db8bb-103">ID3DXMATRIXStack::RotateYawPitchRoll method (D3DX10.h)</span></span>

<span data-ttu-id="db8bb-104">Поворачивает (относительно мирового пространства координат) вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="db8bb-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="db8bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db8bb-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="db8bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db8bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db8bb-107">*Значения нутации* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db8bb-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db8bb-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db8bb-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db8bb-109">Значения нутации вокруг оси y в радианах.</span><span class="sxs-lookup"><span data-stu-id="db8bb-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="db8bb-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db8bb-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db8bb-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db8bb-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db8bb-112">Шаг вокруг оси x в радианах.</span><span class="sxs-lookup"><span data-stu-id="db8bb-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="db8bb-113">*Рулон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db8bb-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db8bb-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db8bb-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db8bb-115">Поворот вокруг оси z в радианах.</span><span class="sxs-lookup"><span data-stu-id="db8bb-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db8bb-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db8bb-116">Return value</span></span>

<span data-ttu-id="db8bb-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db8bb-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db8bb-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="db8bb-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="db8bb-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="db8bb-119">Remarks</span></span>

<span data-ttu-id="db8bb-120">Этот метод добавляет поворот в стек матриц с помощью вычисленной матрицы вращения, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="db8bb-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="db8bb-121">Так как поворот разворачивается вправо до стека матрицы, вращение происходит относительно пространства координат мира.</span><span class="sxs-lookup"><span data-stu-id="db8bb-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="db8bb-122">Требования</span><span class="sxs-lookup"><span data-stu-id="db8bb-122">Requirements</span></span>



| <span data-ttu-id="db8bb-123">Требование</span><span class="sxs-lookup"><span data-stu-id="db8bb-123">Requirement</span></span> | <span data-ttu-id="db8bb-124">Значение</span><span class="sxs-lookup"><span data-stu-id="db8bb-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db8bb-125">Header</span><span class="sxs-lookup"><span data-stu-id="db8bb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="db8bb-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="db8bb-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="db8bb-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="db8bb-127">Library</span></span><br/> | <dl> <span data-ttu-id="db8bb-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db8bb-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db8bb-129">См. также</span><span class="sxs-lookup"><span data-stu-id="db8bb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db8bb-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="db8bb-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="db8bb-131">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="db8bb-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
