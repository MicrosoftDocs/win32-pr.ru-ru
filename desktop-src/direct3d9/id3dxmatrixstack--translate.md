---
description: 'Метод ID3DXMATRIXStack:: Translation (D3dx9math. h) — определяет продукт текущей матрицы и вычисленную матрицу смещения, определяемую заданными факторами (x, y и z).'
ms.assetid: e0ac72a2-9970-433e-9026-aa79edc8261c
title: 'Метод ID3DXMATRIXStack:: сдвиг (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7fadad95e8e72691a0e030ed89eedc745de2be43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093342"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a><span data-ttu-id="e3b19-103">Метод ID3DXMATRIXStack:: сдвиг (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e3b19-103">ID3DXMATRIXStack::Translate method (D3dx9math.h)</span></span>

<span data-ttu-id="e3b19-104">Определяет продукт текущей матрицы и вычисленную матрицу смещения, определяемую заданными факторами (x, y и z).</span><span class="sxs-lookup"><span data-stu-id="e3b19-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b19-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3b19-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="e3b19-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3b19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b19-107">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e3b19-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b19-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b19-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3b19-109">Коэффициент перевода по оси x.</span><span class="sxs-lookup"><span data-stu-id="e3b19-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="e3b19-110">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e3b19-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b19-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b19-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3b19-112">Коэффициент преобразования в направлении y.</span><span class="sxs-lookup"><span data-stu-id="e3b19-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="e3b19-113">*z* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e3b19-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b19-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b19-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3b19-115">Коэффициент перевода в направлении z.</span><span class="sxs-lookup"><span data-stu-id="e3b19-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3b19-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3b19-116">Return value</span></span>

<span data-ttu-id="e3b19-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3b19-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3b19-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e3b19-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3b19-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="e3b19-119">Remarks</span></span>

<span data-ttu-id="e3b19-120">Этот метод дает право на Умножение текущей матрицы на вычисленную матрицу перевода (преобразование относится к текущему источнику мира).</span><span class="sxs-lookup"><span data-stu-id="e3b19-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="e3b19-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e3b19-121">Requirements</span></span>



| <span data-ttu-id="e3b19-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e3b19-122">Requirement</span></span> | <span data-ttu-id="e3b19-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e3b19-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b19-124">Header</span><span class="sxs-lookup"><span data-stu-id="e3b19-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e3b19-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3b19-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e3b19-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e3b19-126">Library</span></span><br/> | <dl> <span data-ttu-id="e3b19-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3b19-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3b19-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e3b19-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b19-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="e3b19-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="e3b19-130">**ID3DXMATRIXStack:: Транслателокал**</span><span class="sxs-lookup"><span data-stu-id="e3b19-130">**ID3DXMATRIXStack::TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
