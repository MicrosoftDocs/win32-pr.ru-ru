---
description: 'Метод ID3DXConstantTable:: Сетматрикспоинтераррай — устанавливает массив указателей на матрицы нонтранспосед.'
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
ms.openlocfilehash: bd9505f82674efc822d4921d7116c8eab17198c1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115072"
---
# <a name="id3dxconstanttablesetmatrixpointerarray-method"></a><span data-ttu-id="0b931-103">Метод ID3DXConstantTable:: Сетматрикспоинтераррай</span><span class="sxs-lookup"><span data-stu-id="0b931-103">ID3DXConstantTable::SetMatrixPointerArray method</span></span>

<span data-ttu-id="0b931-104">Задает массив указателей для нонтранспосед матриц.</span><span class="sxs-lookup"><span data-stu-id="0b931-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b931-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b931-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="0b931-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b931-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b931-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0b931-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b931-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0b931-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0b931-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="0b931-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="0b931-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0b931-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b931-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0b931-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0b931-112">Уникальный идентификатор массива константных матриц.</span><span class="sxs-lookup"><span data-stu-id="0b931-112">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="0b931-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0b931-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b931-114">*ппматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0b931-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b931-115">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="0b931-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="0b931-116">Массив указателей на матрицы нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="0b931-116">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="0b931-117">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="0b931-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b931-118">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0b931-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b931-119">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b931-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b931-120">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="0b931-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b931-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b931-121">Return value</span></span>

<span data-ttu-id="0b931-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b931-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b931-123">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0b931-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0b931-124">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="0b931-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b931-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="0b931-125">Remarks</span></span>

<span data-ttu-id="0b931-126">Матрица нонтранспосед содержит основные данные строки. то есть каждый вектор содержится в строке.</span><span class="sxs-lookup"><span data-stu-id="0b931-126">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b931-127">Требования</span><span class="sxs-lookup"><span data-stu-id="0b931-127">Requirements</span></span>



| <span data-ttu-id="0b931-128">Требование</span><span class="sxs-lookup"><span data-stu-id="0b931-128">Requirement</span></span> | <span data-ttu-id="0b931-129">Значение</span><span class="sxs-lookup"><span data-stu-id="0b931-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b931-130">Header</span><span class="sxs-lookup"><span data-stu-id="0b931-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0b931-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b931-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0b931-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0b931-132">Library</span></span><br/> | <dl> <span data-ttu-id="0b931-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b931-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0b931-134">См. также</span><span class="sxs-lookup"><span data-stu-id="0b931-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b931-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="0b931-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
