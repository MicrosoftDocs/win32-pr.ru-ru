---
description: 'Метод ID3DXConstantTable:: Сетматриксаррай — задает массив матриц нонтранспосед.'
ms.assetid: f36b8e8a-c22f-41e6-acb1-6298291b002f
title: 'Метод ID3DXConstantTable:: Сетматриксаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 02e115cf4526ab065d2613636427059826f450f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115102"
---
# <a name="id3dxconstanttablesetmatrixarray-method"></a><span data-ttu-id="23f65-103">Метод ID3DXConstantTable:: Сетматриксаррай</span><span class="sxs-lookup"><span data-stu-id="23f65-103">ID3DXConstantTable::SetMatrixArray method</span></span>

<span data-ttu-id="23f65-104">Задает массив матриц нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="23f65-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f65-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23f65-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="23f65-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="23f65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23f65-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23f65-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23f65-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="23f65-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="23f65-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="23f65-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="23f65-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23f65-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23f65-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="23f65-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="23f65-112">Уникальный идентификатор массива константных матриц.</span><span class="sxs-lookup"><span data-stu-id="23f65-112">Unique identifier to the array of constant matrices.</span></span> <span data-ttu-id="23f65-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="23f65-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="23f65-114">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23f65-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23f65-115">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="23f65-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="23f65-116">Массив матриц нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="23f65-116">Array of nontransposed matrices.</span></span> <span data-ttu-id="23f65-117">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="23f65-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="23f65-118">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23f65-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23f65-119">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23f65-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23f65-120">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="23f65-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23f65-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23f65-121">Return value</span></span>

<span data-ttu-id="23f65-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23f65-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23f65-123">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="23f65-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="23f65-124">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="23f65-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="23f65-125">Требования</span><span class="sxs-lookup"><span data-stu-id="23f65-125">Requirements</span></span>



| <span data-ttu-id="23f65-126">Требование</span><span class="sxs-lookup"><span data-stu-id="23f65-126">Requirement</span></span> | <span data-ttu-id="23f65-127">Значение</span><span class="sxs-lookup"><span data-stu-id="23f65-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="23f65-128">Header</span><span class="sxs-lookup"><span data-stu-id="23f65-128">Header</span></span><br/>  | <dl> <span data-ttu-id="23f65-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="23f65-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="23f65-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="23f65-130">Library</span></span><br/> | <dl> <span data-ttu-id="23f65-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23f65-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="23f65-132">См. также</span><span class="sxs-lookup"><span data-stu-id="23f65-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f65-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="23f65-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
