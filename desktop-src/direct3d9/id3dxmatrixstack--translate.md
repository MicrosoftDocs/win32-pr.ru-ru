---
description: Определяет продукт текущей матрицы и вычисленную матрицу смещения, определяемую заданными факторами (x, y и z).
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
ms.openlocfilehash: 228b4302a512e96d5c009edcb3f0b673ee61e047
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704029"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a><span data-ttu-id="efde2-103">Метод ID3DXMATRIXStack:: сдвиг (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="efde2-103">ID3DXMATRIXStack::Translate method (D3dx9math.h)</span></span>

<span data-ttu-id="efde2-104">Определяет продукт текущей матрицы и вычисленную матрицу смещения, определяемую заданными факторами (x, y и z).</span><span class="sxs-lookup"><span data-stu-id="efde2-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="efde2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efde2-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="efde2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="efde2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efde2-107">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="efde2-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efde2-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="efde2-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="efde2-109">Коэффициент перевода по оси x.</span><span class="sxs-lookup"><span data-stu-id="efde2-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="efde2-110">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="efde2-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efde2-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="efde2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="efde2-112">Коэффициент преобразования в направлении y.</span><span class="sxs-lookup"><span data-stu-id="efde2-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="efde2-113">*z* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="efde2-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efde2-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="efde2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="efde2-115">Коэффициент перевода в направлении z.</span><span class="sxs-lookup"><span data-stu-id="efde2-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efde2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efde2-116">Return value</span></span>

<span data-ttu-id="efde2-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="efde2-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="efde2-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="efde2-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="efde2-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="efde2-119">Remarks</span></span>

<span data-ttu-id="efde2-120">Этот метод дает право на Умножение текущей матрицы на вычисленную матрицу перевода (преобразование относится к текущему источнику мира).</span><span class="sxs-lookup"><span data-stu-id="efde2-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="efde2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="efde2-121">Requirements</span></span>



| <span data-ttu-id="efde2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="efde2-122">Requirement</span></span> | <span data-ttu-id="efde2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="efde2-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="efde2-124">Header</span><span class="sxs-lookup"><span data-stu-id="efde2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="efde2-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="efde2-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="efde2-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="efde2-126">Library</span></span><br/> | <dl> <span data-ttu-id="efde2-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efde2-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="efde2-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efde2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efde2-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="efde2-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="efde2-130">**ID3DXMATRIXStack:: Транслателокал**</span><span class="sxs-lookup"><span data-stu-id="efde2-130">**ID3DXMATRIXStack::TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
