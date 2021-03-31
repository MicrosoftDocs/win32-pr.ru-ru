---
description: Масштабировать текущую матрицу относительно источника объекта.
ms.assetid: fe71da67-c8c9-4c78-9055-9bc3cadc0780
title: 'Метод ID3DXMATRIXStack:: Скалелокал (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.ScaleLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05b188e3f1b0322225584bc0ef7c194c52ef949f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273725"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx9mathh"></a><span data-ttu-id="002e2-103">Метод ID3DXMATRIXStack:: Скалелокал (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="002e2-103">ID3DXMATRIXStack::ScaleLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="002e2-104">Масштабировать текущую матрицу относительно источника объекта.</span><span class="sxs-lookup"><span data-stu-id="002e2-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="002e2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="002e2-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="002e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="002e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="002e2-107">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="002e2-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002e2-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="002e2-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="002e2-109">Компонент масштабирования по оси x.</span><span class="sxs-lookup"><span data-stu-id="002e2-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="002e2-110">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="002e2-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002e2-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="002e2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="002e2-112">Компонент масштабирования в направлении y.</span><span class="sxs-lookup"><span data-stu-id="002e2-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="002e2-113">*z* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="002e2-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002e2-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="002e2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="002e2-115">Компонент масштабирования в направлении z.</span><span class="sxs-lookup"><span data-stu-id="002e2-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="002e2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="002e2-116">Return value</span></span>

<span data-ttu-id="002e2-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="002e2-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="002e2-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="002e2-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="002e2-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="002e2-119">Remarks</span></span>

<span data-ttu-id="002e2-120">Этот метод Left — Умножает текущую матрицу на вычисленную матрицу масштабирования.</span><span class="sxs-lookup"><span data-stu-id="002e2-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="002e2-121">Преобразование относится к локальному источнику объекта.</span><span class="sxs-lookup"><span data-stu-id="002e2-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="002e2-122">Требования</span><span class="sxs-lookup"><span data-stu-id="002e2-122">Requirements</span></span>



| <span data-ttu-id="002e2-123">Требование</span><span class="sxs-lookup"><span data-stu-id="002e2-123">Requirement</span></span> | <span data-ttu-id="002e2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="002e2-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="002e2-125">Header</span><span class="sxs-lookup"><span data-stu-id="002e2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="002e2-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="002e2-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="002e2-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="002e2-127">Library</span></span><br/> | <dl> <span data-ttu-id="002e2-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="002e2-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="002e2-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="002e2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="002e2-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="002e2-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="002e2-131">**ID3DXMATRIXStack:: Scale**</span><span class="sxs-lookup"><span data-stu-id="002e2-131">**ID3DXMATRIXStack::Scale**</span></span>](id3dxmatrixstack--scale.md)
</dt> </dl>

 

 
