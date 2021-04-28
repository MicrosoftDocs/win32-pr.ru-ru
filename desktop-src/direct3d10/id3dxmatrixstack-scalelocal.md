---
description: 'Метод ID3DXMATRIXStack:: Скалелокал (D3DX10. h) — масштабирование текущей матрицы относительно источника объекта.'
ms.assetid: 748fce3a-a33c-4975-bbf0-dd3167a036f1
title: 'Метод ID3DXMATRIXStack:: Скалелокал (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3961db0794703e3974dbd92d8eae8293173c2354
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107782"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx10h"></a><span data-ttu-id="46d5f-103">Метод ID3DXMATRIXStack:: Скалелокал (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="46d5f-103">ID3DXMATRIXStack::ScaleLocal method (D3DX10.h)</span></span>

<span data-ttu-id="46d5f-104">Масштабировать текущую матрицу относительно источника объекта.</span><span class="sxs-lookup"><span data-stu-id="46d5f-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="46d5f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46d5f-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="46d5f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="46d5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46d5f-107">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="46d5f-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46d5f-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46d5f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46d5f-109">Компонент масштабирования по оси x.</span><span class="sxs-lookup"><span data-stu-id="46d5f-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="46d5f-110">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="46d5f-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46d5f-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46d5f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46d5f-112">Компонент масштабирования в направлении y.</span><span class="sxs-lookup"><span data-stu-id="46d5f-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="46d5f-113">*z* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="46d5f-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46d5f-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46d5f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46d5f-115">Компонент масштабирования в направлении z.</span><span class="sxs-lookup"><span data-stu-id="46d5f-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46d5f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46d5f-116">Return value</span></span>

<span data-ttu-id="46d5f-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46d5f-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46d5f-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="46d5f-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="46d5f-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="46d5f-119">Remarks</span></span>

<span data-ttu-id="46d5f-120">Этот метод Left — Умножает текущую матрицу на вычисленную матрицу масштабирования.</span><span class="sxs-lookup"><span data-stu-id="46d5f-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="46d5f-121">Преобразование относится к локальному источнику объекта.</span><span class="sxs-lookup"><span data-stu-id="46d5f-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="46d5f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="46d5f-122">Requirements</span></span>



| <span data-ttu-id="46d5f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="46d5f-123">Requirement</span></span> | <span data-ttu-id="46d5f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="46d5f-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46d5f-125">Header</span><span class="sxs-lookup"><span data-stu-id="46d5f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="46d5f-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="46d5f-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="46d5f-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="46d5f-127">Library</span></span><br/> | <dl> <span data-ttu-id="46d5f-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46d5f-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46d5f-129">См. также</span><span class="sxs-lookup"><span data-stu-id="46d5f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d5f-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="46d5f-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="46d5f-131">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="46d5f-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
