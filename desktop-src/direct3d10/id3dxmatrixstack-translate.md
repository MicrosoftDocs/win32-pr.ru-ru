---
description: Определяет продукт текущей матрицы и вычисленную матрицу смещения, определяемую заданными факторами (x, y и z).
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
ms.openlocfilehash: 159e1dc6b3dabeb92b32798cbe318f6c72c01d70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704007"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx10h"></a><span data-ttu-id="40150-103">Метод ID3DXMATRIXStack:: сдвиг (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="40150-103">ID3DXMATRIXStack::Translate method (D3DX10.h)</span></span>

<span data-ttu-id="40150-104">Определяет продукт текущей матрицы и вычисленную матрицу смещения, определяемую заданными факторами (x, y и z).</span><span class="sxs-lookup"><span data-stu-id="40150-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="40150-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40150-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="40150-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="40150-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40150-107">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="40150-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40150-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40150-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40150-109">Коэффициент перевода по оси x.</span><span class="sxs-lookup"><span data-stu-id="40150-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="40150-110">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="40150-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40150-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40150-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40150-112">Коэффициент преобразования в направлении y.</span><span class="sxs-lookup"><span data-stu-id="40150-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="40150-113">*z* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="40150-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40150-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40150-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40150-115">Коэффициент перевода в направлении z.</span><span class="sxs-lookup"><span data-stu-id="40150-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40150-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40150-116">Return value</span></span>

<span data-ttu-id="40150-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="40150-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="40150-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="40150-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="40150-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40150-119">Remarks</span></span>

<span data-ttu-id="40150-120">Этот метод дает право на Умножение текущей матрицы на вычисленную матрицу перевода (преобразование относится к текущему источнику мира).</span><span class="sxs-lookup"><span data-stu-id="40150-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="40150-121">Требования</span><span class="sxs-lookup"><span data-stu-id="40150-121">Requirements</span></span>



| <span data-ttu-id="40150-122">Требование</span><span class="sxs-lookup"><span data-stu-id="40150-122">Requirement</span></span> | <span data-ttu-id="40150-123">Значение</span><span class="sxs-lookup"><span data-stu-id="40150-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40150-124">Header</span><span class="sxs-lookup"><span data-stu-id="40150-124">Header</span></span><br/>  | <dl> <span data-ttu-id="40150-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="40150-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="40150-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="40150-126">Library</span></span><br/> | <dl> <span data-ttu-id="40150-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40150-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40150-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40150-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40150-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="40150-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="40150-130">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="40150-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
