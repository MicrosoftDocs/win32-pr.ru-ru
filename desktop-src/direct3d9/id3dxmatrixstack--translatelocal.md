---
description: Определяет продукт вычисленной матрицы перевода, определяемый заданными факторами (x, y и z) и текущей матрицей.
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
ms.openlocfilehash: 784e623ae47dfece9b395d423437fb6ce661b223
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273858"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx9mathh"></a><span data-ttu-id="a714b-103">Метод ID3DXMATRIXStack:: Транслателокал (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a714b-103">ID3DXMATRIXStack::TranslateLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="a714b-104">Определяет продукт вычисленной матрицы перевода, определяемый заданными факторами (x, y и z) и текущей матрицей.</span><span class="sxs-lookup"><span data-stu-id="a714b-104">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a714b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a714b-105">Syntax</span></span>


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="a714b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a714b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a714b-107">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a714b-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a714b-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a714b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a714b-109">Коэффициент перевода по оси x.</span><span class="sxs-lookup"><span data-stu-id="a714b-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="a714b-110">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a714b-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a714b-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a714b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a714b-112">Коэффициент преобразования в направлении y.</span><span class="sxs-lookup"><span data-stu-id="a714b-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="a714b-113">*z* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a714b-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a714b-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a714b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a714b-115">Коэффициент перевода в направлении z.</span><span class="sxs-lookup"><span data-stu-id="a714b-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a714b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a714b-116">Return value</span></span>

<span data-ttu-id="a714b-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a714b-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a714b-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a714b-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a714b-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a714b-119">Remarks</span></span>

<span data-ttu-id="a714b-120">Этот метод Left — Умножает текущую матрицу на вычисленную матрицу перевода (преобразование относится к локальному источнику объекта).</span><span class="sxs-lookup"><span data-stu-id="a714b-120">This method left-multiplies the current matrix with the computed translation matrix (transformation is about the local origin of the object).</span></span>


```
    
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="a714b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a714b-121">Requirements</span></span>



| <span data-ttu-id="a714b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a714b-122">Requirement</span></span> | <span data-ttu-id="a714b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a714b-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a714b-124">Header</span><span class="sxs-lookup"><span data-stu-id="a714b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a714b-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a714b-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a714b-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a714b-126">Library</span></span><br/> | <dl> <span data-ttu-id="a714b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a714b-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a714b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a714b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a714b-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="a714b-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="a714b-130">**ID3DXMATRIXStack:: сдвиг**</span><span class="sxs-lookup"><span data-stu-id="a714b-130">**ID3DXMATRIXStack::Translate**</span></span>](id3dxmatrixstack--translate.md)
</dt> </dl>

 

 
