---
description: 'Метод ID3DXMATRIXStack:: Translation (D3DX10. h) — определяет продукт текущей матрицы и вычисленную матрицу смещения, определяемую заданными факторами (x, y и z).'
ms.assetid: d6e347a5-bb66-451d-b66e-49ea8eff70b3
title: 'Метод ID3DXMATRIXStack:: сдвиг (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 41e84b62c077da03806a5e781498c05ee3c8ee67
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107772"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx10h"></a><span data-ttu-id="1853d-103">Метод ID3DXMATRIXStack:: сдвиг (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="1853d-103">ID3DXMATRIXStack::Translate method (D3DX10.h)</span></span>

<span data-ttu-id="1853d-104">Определяет продукт текущей матрицы и вычисленную матрицу смещения, определяемую заданными факторами (x, y и z).</span><span class="sxs-lookup"><span data-stu-id="1853d-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="1853d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1853d-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="1853d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1853d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1853d-107">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="1853d-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1853d-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1853d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1853d-109">Коэффициент перевода по оси x.</span><span class="sxs-lookup"><span data-stu-id="1853d-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="1853d-110">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="1853d-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1853d-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1853d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1853d-112">Коэффициент преобразования в направлении y.</span><span class="sxs-lookup"><span data-stu-id="1853d-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="1853d-113">*z* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="1853d-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1853d-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1853d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1853d-115">Коэффициент перевода в направлении z.</span><span class="sxs-lookup"><span data-stu-id="1853d-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1853d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1853d-116">Return value</span></span>

<span data-ttu-id="1853d-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1853d-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1853d-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1853d-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1853d-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="1853d-119">Remarks</span></span>

<span data-ttu-id="1853d-120">Этот метод дает право на Умножение текущей матрицы на вычисленную матрицу перевода (преобразование относится к текущему источнику мира).</span><span class="sxs-lookup"><span data-stu-id="1853d-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="1853d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1853d-121">Requirements</span></span>



| <span data-ttu-id="1853d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1853d-122">Requirement</span></span> | <span data-ttu-id="1853d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1853d-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1853d-124">Header</span><span class="sxs-lookup"><span data-stu-id="1853d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1853d-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1853d-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1853d-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1853d-126">Library</span></span><br/> | <dl> <span data-ttu-id="1853d-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1853d-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1853d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="1853d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1853d-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="1853d-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="1853d-130">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="1853d-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
