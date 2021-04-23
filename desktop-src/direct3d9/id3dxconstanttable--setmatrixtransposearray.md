---
description: Задает массив переданных матриц.
ms.assetid: a67afc21-f43d-4dc5-b145-f3d66dd86dbb
title: 'Метод ID3DXConstantTable:: Сетматрикстранспосеаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69755ed973a8c412373287f128642b78ea2ad346
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547951"
---
# <a name="id3dxconstanttablesetmatrixtransposearray-method"></a><span data-ttu-id="e90fe-103">Метод ID3DXConstantTable:: Сетматрикстранспосеаррай</span><span class="sxs-lookup"><span data-stu-id="e90fe-103">ID3DXConstantTable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="e90fe-104">Задает массив переданных матриц.</span><span class="sxs-lookup"><span data-stu-id="e90fe-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e90fe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e90fe-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="e90fe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e90fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e90fe-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e90fe-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90fe-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e90fe-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e90fe-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="e90fe-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="e90fe-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e90fe-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90fe-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e90fe-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e90fe-112">Уникальный идентификатор массива констант матрицы.</span><span class="sxs-lookup"><span data-stu-id="e90fe-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="e90fe-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e90fe-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90fe-114">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e90fe-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90fe-115">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e90fe-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e90fe-116">Массив переданных матриц.</span><span class="sxs-lookup"><span data-stu-id="e90fe-116">Array of transposed matrices.</span></span> <span data-ttu-id="e90fe-117">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="e90fe-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="e90fe-118">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e90fe-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90fe-119">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e90fe-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e90fe-120">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="e90fe-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e90fe-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e90fe-121">Return value</span></span>

<span data-ttu-id="e90fe-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e90fe-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e90fe-123">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e90fe-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e90fe-124">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="e90fe-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e90fe-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e90fe-125">Requirements</span></span>



| <span data-ttu-id="e90fe-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e90fe-126">Requirement</span></span> | <span data-ttu-id="e90fe-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e90fe-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e90fe-128">Header</span><span class="sxs-lookup"><span data-stu-id="e90fe-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e90fe-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e90fe-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e90fe-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e90fe-130">Library</span></span><br/> | <dl> <span data-ttu-id="e90fe-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e90fe-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e90fe-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e90fe-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e90fe-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="e90fe-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
