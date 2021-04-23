---
description: Масштабировать текущую матрицу относительно источника координат мира.
ms.assetid: d0f4b341-b3b6-42e4-84df-78f203c3728e
title: 'Метод ID3DXMATRIXStack:: Scale (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Scale
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 361c1fcbdc3f793bcf3e21d569eee740ca0b4ee2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704008"
---
# <a name="id3dxmatrixstackscale-method-d3dx10h"></a><span data-ttu-id="56e43-103">Метод ID3DXMATRIXStack:: Scale (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="56e43-103">ID3DXMATRIXStack::Scale method (D3DX10.h)</span></span>

<span data-ttu-id="56e43-104">Масштабировать текущую матрицу относительно источника координат мира.</span><span class="sxs-lookup"><span data-stu-id="56e43-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e43-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56e43-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="56e43-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="56e43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56e43-107">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="56e43-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56e43-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56e43-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="56e43-109">Компонент масштабирования по оси x.</span><span class="sxs-lookup"><span data-stu-id="56e43-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="56e43-110">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="56e43-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56e43-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56e43-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="56e43-112">Компонент масштабирования в направлении y.</span><span class="sxs-lookup"><span data-stu-id="56e43-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="56e43-113">*z* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="56e43-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56e43-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56e43-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="56e43-115">Компонент масштабирования в направлении z.</span><span class="sxs-lookup"><span data-stu-id="56e43-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56e43-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56e43-116">Return value</span></span>

<span data-ttu-id="56e43-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="56e43-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="56e43-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="56e43-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="56e43-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56e43-119">Remarks</span></span>

<span data-ttu-id="56e43-120">Этот метод дает право на Умножение текущей матрицы на вычисленную матрицу масштабирования.</span><span class="sxs-lookup"><span data-stu-id="56e43-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="56e43-121">Преобразование относится к текущему источнику мира.</span><span class="sxs-lookup"><span data-stu-id="56e43-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="56e43-122">Требования</span><span class="sxs-lookup"><span data-stu-id="56e43-122">Requirements</span></span>



| <span data-ttu-id="56e43-123">Требование</span><span class="sxs-lookup"><span data-stu-id="56e43-123">Requirement</span></span> | <span data-ttu-id="56e43-124">Значение</span><span class="sxs-lookup"><span data-stu-id="56e43-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56e43-125">Header</span><span class="sxs-lookup"><span data-stu-id="56e43-125">Header</span></span><br/>  | <dl> <span data-ttu-id="56e43-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="56e43-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="56e43-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="56e43-127">Library</span></span><br/> | <dl> <span data-ttu-id="56e43-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56e43-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56e43-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56e43-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e43-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="56e43-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="56e43-131">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="56e43-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
