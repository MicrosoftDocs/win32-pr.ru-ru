---
description: Задает массив указателей для нонтранспосед матриц.
ms.assetid: 1b985e03-b5cb-48e5-969f-115ca165acdc
title: 'Метод ID3DXConstantTable:: Сетматрикспоинтераррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b29d4298d8ca52d2826cc780fb90d769c3337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703812"
---
# <a name="id3dxconstanttablesetmatrixpointerarray-method"></a><span data-ttu-id="a0621-103">Метод ID3DXConstantTable:: Сетматрикспоинтераррай</span><span class="sxs-lookup"><span data-stu-id="a0621-103">ID3DXConstantTable::SetMatrixPointerArray method</span></span>

<span data-ttu-id="a0621-104">Задает массив указателей для нонтранспосед матриц.</span><span class="sxs-lookup"><span data-stu-id="a0621-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0621-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0621-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="a0621-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0621-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0621-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0621-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0621-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a0621-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a0621-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="a0621-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="a0621-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0621-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0621-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a0621-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a0621-112">Уникальный идентификатор массива константных матриц.</span><span class="sxs-lookup"><span data-stu-id="a0621-112">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="a0621-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a0621-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0621-114">*ппматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0621-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0621-115">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="a0621-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="a0621-116">Массив указателей на матрицы нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="a0621-116">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="a0621-117">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="a0621-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0621-118">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0621-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0621-119">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0621-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0621-120">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="a0621-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0621-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0621-121">Return value</span></span>

<span data-ttu-id="a0621-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0621-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0621-123">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a0621-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a0621-124">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="a0621-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0621-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0621-125">Remarks</span></span>

<span data-ttu-id="a0621-126">Матрица нонтранспосед содержит основные данные строки. то есть каждый вектор содержится в строке.</span><span class="sxs-lookup"><span data-stu-id="a0621-126">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0621-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a0621-127">Requirements</span></span>



| <span data-ttu-id="a0621-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a0621-128">Requirement</span></span> | <span data-ttu-id="a0621-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a0621-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0621-130">Header</span><span class="sxs-lookup"><span data-stu-id="a0621-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a0621-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0621-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a0621-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a0621-132">Library</span></span><br/> | <dl> <span data-ttu-id="a0621-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0621-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a0621-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0621-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0621-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="a0621-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
