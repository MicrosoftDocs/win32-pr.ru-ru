---
description: 'Метод ID3DXMATRIXStack:: Scale (D3dx9math. h). масштабирование текущей матрицы относительно источника координат мира.'
ms.assetid: 6c4ef625-736e-41a0-8a79-4d71e8685754
title: 'Метод ID3DXMATRIXStack:: Scale (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d877fccf5bfebfdc1f9cf3943c4334e5b8c7fff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093372"
---
# <a name="id3dxmatrixstackscale-method-d3dx9mathh"></a><span data-ttu-id="4742a-103">Метод ID3DXMATRIXStack:: Scale (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="4742a-103">ID3DXMATRIXStack::Scale method (D3dx9math.h)</span></span>

<span data-ttu-id="4742a-104">Масштабировать текущую матрицу относительно источника координат мира.</span><span class="sxs-lookup"><span data-stu-id="4742a-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="4742a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4742a-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="4742a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4742a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4742a-107">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="4742a-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4742a-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4742a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4742a-109">Компонент масштабирования по оси x.</span><span class="sxs-lookup"><span data-stu-id="4742a-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="4742a-110">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="4742a-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4742a-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4742a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4742a-112">Компонент масштабирования в направлении y.</span><span class="sxs-lookup"><span data-stu-id="4742a-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="4742a-113">*z* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="4742a-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4742a-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4742a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4742a-115">Компонент масштабирования в направлении z.</span><span class="sxs-lookup"><span data-stu-id="4742a-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4742a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4742a-116">Return value</span></span>

<span data-ttu-id="4742a-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4742a-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4742a-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4742a-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4742a-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="4742a-119">Remarks</span></span>

<span data-ttu-id="4742a-120">Этот метод дает право на Умножение текущей матрицы на вычисленную матрицу масштабирования.</span><span class="sxs-lookup"><span data-stu-id="4742a-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="4742a-121">Преобразование относится к текущему источнику мира.</span><span class="sxs-lookup"><span data-stu-id="4742a-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="4742a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4742a-122">Requirements</span></span>



| <span data-ttu-id="4742a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4742a-123">Requirement</span></span> | <span data-ttu-id="4742a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4742a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4742a-125">Header</span><span class="sxs-lookup"><span data-stu-id="4742a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4742a-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4742a-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4742a-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4742a-127">Library</span></span><br/> | <dl> <span data-ttu-id="4742a-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4742a-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4742a-129">См. также</span><span class="sxs-lookup"><span data-stu-id="4742a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4742a-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="4742a-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="4742a-131">**ID3DXMATRIXStack:: Скалелокал**</span><span class="sxs-lookup"><span data-stu-id="4742a-131">**ID3DXMATRIXStack::ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)
</dt> </dl>

 

 
