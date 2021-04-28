---
description: 'Метод ID3DXMATRIXStack:: Транслателокал (D3dx9math. h) — определяет продукт вычисленной матрицы перевода, определяемый заданными факторами (x, y и z) и текущей матрицей.'
ms.assetid: d4752a6c-2114-4016-a69f-dcc561d2c76b
title: 'Метод ID3DXMATRIXStack:: Транслателокал (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b9badd4b01d1245247766c750e2a2ea1f266d9e1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107372"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx9mathh"></a><span data-ttu-id="3773f-103">Метод ID3DXMATRIXStack:: Транслателокал (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="3773f-103">ID3DXMATRIXStack::TranslateLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="3773f-104">Определяет продукт вычисленной матрицы перевода, определяемый заданными факторами (x, y и z) и текущей матрицей.</span><span class="sxs-lookup"><span data-stu-id="3773f-104">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="3773f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3773f-105">Syntax</span></span>


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="3773f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3773f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3773f-107">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3773f-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3773f-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3773f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3773f-109">Коэффициент перевода по оси x.</span><span class="sxs-lookup"><span data-stu-id="3773f-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="3773f-110">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3773f-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3773f-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3773f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3773f-112">Коэффициент преобразования в направлении y.</span><span class="sxs-lookup"><span data-stu-id="3773f-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="3773f-113">*z* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3773f-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3773f-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3773f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3773f-115">Коэффициент перевода в направлении z.</span><span class="sxs-lookup"><span data-stu-id="3773f-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3773f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3773f-116">Return value</span></span>

<span data-ttu-id="3773f-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3773f-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3773f-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3773f-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3773f-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="3773f-119">Remarks</span></span>

<span data-ttu-id="3773f-120">Этот метод Left — Умножает текущую матрицу на вычисленную матрицу перевода (преобразование относится к локальному источнику объекта).</span><span class="sxs-lookup"><span data-stu-id="3773f-120">This method left-multiplies the current matrix with the computed translation matrix (transformation is about the local origin of the object).</span></span>


```
    
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="3773f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="3773f-121">Requirements</span></span>



| <span data-ttu-id="3773f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="3773f-122">Requirement</span></span> | <span data-ttu-id="3773f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3773f-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3773f-124">Header</span><span class="sxs-lookup"><span data-stu-id="3773f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3773f-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3773f-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3773f-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3773f-126">Library</span></span><br/> | <dl> <span data-ttu-id="3773f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3773f-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3773f-128">См. также</span><span class="sxs-lookup"><span data-stu-id="3773f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3773f-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="3773f-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="3773f-130">**ID3DXMATRIXStack:: сдвиг**</span><span class="sxs-lookup"><span data-stu-id="3773f-130">**ID3DXMATRIXStack::Translate**</span></span>](id3dxmatrixstack--translate.md)
</dt> </dl>

 

 
