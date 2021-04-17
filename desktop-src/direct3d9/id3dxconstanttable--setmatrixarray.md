---
description: Задает массив матриц нонтранспосед.
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
ms.openlocfilehash: 48dd85975ac58dd26d4194584ce5fbebe26da2a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703815"
---
# <a name="id3dxconstanttablesetmatrixarray-method"></a><span data-ttu-id="3e4de-103">Метод ID3DXConstantTable:: Сетматриксаррай</span><span class="sxs-lookup"><span data-stu-id="3e4de-103">ID3DXConstantTable::SetMatrixArray method</span></span>

<span data-ttu-id="3e4de-104">Задает массив матриц нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="3e4de-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e4de-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e4de-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="3e4de-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e4de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e4de-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e4de-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4de-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="3e4de-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="3e4de-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="3e4de-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="3e4de-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e4de-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4de-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="3e4de-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="3e4de-112">Уникальный идентификатор массива константных матриц.</span><span class="sxs-lookup"><span data-stu-id="3e4de-112">Unique identifier to the array of constant matrices.</span></span> <span data-ttu-id="3e4de-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3e4de-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e4de-114">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e4de-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4de-115">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3e4de-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3e4de-116">Массив матриц нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="3e4de-116">Array of nontransposed matrices.</span></span> <span data-ttu-id="3e4de-117">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="3e4de-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e4de-118">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e4de-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4de-119">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e4de-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e4de-120">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="3e4de-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e4de-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e4de-121">Return value</span></span>

<span data-ttu-id="3e4de-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3e4de-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3e4de-123">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3e4de-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3e4de-124">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="3e4de-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e4de-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3e4de-125">Requirements</span></span>



| <span data-ttu-id="3e4de-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3e4de-126">Requirement</span></span> | <span data-ttu-id="3e4de-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3e4de-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e4de-128">Header</span><span class="sxs-lookup"><span data-stu-id="3e4de-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3e4de-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e4de-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3e4de-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3e4de-130">Library</span></span><br/> | <dl> <span data-ttu-id="3e4de-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e4de-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3e4de-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e4de-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e4de-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="3e4de-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
