---
description: Определяет продукт вычисленной матрицы перевода, определяемый заданными факторами (x, y и z) и текущей матрицей.
ms.assetid: 96399801-dd80-4e9a-a5c3-c5d41eb9368a
title: 'Метод ID3DXMATRIXStack:: Транслателокал (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 65a627141f552107d88c3f43988daa0d316a0bef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674757"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx10h"></a><span data-ttu-id="3f044-103">Метод ID3DXMATRIXStack:: Транслателокал (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="3f044-103">ID3DXMATRIXStack::TranslateLocal method (D3DX10.h)</span></span>

<span data-ttu-id="3f044-104">Определяет продукт вычисленной матрицы перевода, определяемый заданными факторами (x, y и z) и текущей матрицей.</span><span class="sxs-lookup"><span data-stu-id="3f044-104">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f044-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f044-105">Syntax</span></span>


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="3f044-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f044-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f044-107">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3f044-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f044-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f044-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f044-109">Коэффициент перевода по оси x.</span><span class="sxs-lookup"><span data-stu-id="3f044-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="3f044-110">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3f044-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f044-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f044-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f044-112">Коэффициент преобразования в направлении y.</span><span class="sxs-lookup"><span data-stu-id="3f044-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="3f044-113">*z* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3f044-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f044-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f044-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f044-115">Коэффициент перевода в направлении z.</span><span class="sxs-lookup"><span data-stu-id="3f044-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f044-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f044-116">Return value</span></span>

<span data-ttu-id="3f044-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3f044-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3f044-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3f044-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f044-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f044-119">Remarks</span></span>

<span data-ttu-id="3f044-120">Этот метод Left — Умножает текущую матрицу на вычисленную матрицу перевода (преобразование относится к локальному источнику объекта).</span><span class="sxs-lookup"><span data-stu-id="3f044-120">This method left-multiplies the current matrix with the computed translation matrix (transformation is about the local origin of the object).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation(&tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="3f044-121">Требования</span><span class="sxs-lookup"><span data-stu-id="3f044-121">Requirements</span></span>



| <span data-ttu-id="3f044-122">Требование</span><span class="sxs-lookup"><span data-stu-id="3f044-122">Requirement</span></span> | <span data-ttu-id="3f044-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3f044-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f044-124">Header</span><span class="sxs-lookup"><span data-stu-id="3f044-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3f044-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f044-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f044-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3f044-126">Library</span></span><br/> | <dl> <span data-ttu-id="3f044-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f044-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f044-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f044-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f044-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="3f044-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="3f044-130">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="3f044-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
