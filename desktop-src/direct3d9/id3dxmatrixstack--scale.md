---
description: Масштабировать текущую матрицу относительно источника координат мира.
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
ms.openlocfilehash: 5ed926a55c0dba6f74e819cd89a7fa75f6d087c4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157143"
---
# <a name="id3dxmatrixstackscale-method-d3dx9mathh"></a><span data-ttu-id="ff580-103">Метод ID3DXMATRIXStack:: Scale (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ff580-103">ID3DXMATRIXStack::Scale method (D3dx9math.h)</span></span>

<span data-ttu-id="ff580-104">Масштабировать текущую матрицу относительно источника координат мира.</span><span class="sxs-lookup"><span data-stu-id="ff580-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff580-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff580-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="ff580-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff580-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff580-107">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="ff580-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff580-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff580-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff580-109">Компонент масштабирования по оси x.</span><span class="sxs-lookup"><span data-stu-id="ff580-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="ff580-110">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="ff580-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff580-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff580-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff580-112">Компонент масштабирования в направлении y.</span><span class="sxs-lookup"><span data-stu-id="ff580-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="ff580-113">*z* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="ff580-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff580-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff580-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff580-115">Компонент масштабирования в направлении z.</span><span class="sxs-lookup"><span data-stu-id="ff580-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff580-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff580-116">Return value</span></span>

<span data-ttu-id="ff580-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ff580-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ff580-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ff580-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff580-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff580-119">Remarks</span></span>

<span data-ttu-id="ff580-120">Этот метод дает право на Умножение текущей матрицы на вычисленную матрицу масштабирования.</span><span class="sxs-lookup"><span data-stu-id="ff580-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="ff580-121">Преобразование относится к текущему источнику мира.</span><span class="sxs-lookup"><span data-stu-id="ff580-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="ff580-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ff580-122">Requirements</span></span>



| <span data-ttu-id="ff580-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ff580-123">Requirement</span></span> | <span data-ttu-id="ff580-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ff580-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff580-125">Header</span><span class="sxs-lookup"><span data-stu-id="ff580-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ff580-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff580-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ff580-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ff580-127">Library</span></span><br/> | <dl> <span data-ttu-id="ff580-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff580-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ff580-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff580-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff580-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="ff580-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="ff580-131">**ID3DXMATRIXStack:: Скалелокал**</span><span class="sxs-lookup"><span data-stu-id="ff580-131">**ID3DXMATRIXStack::ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)
</dt> </dl>

 

 
