---
description: Задает массив указателей на перекладываемые матрицы.
ms.assetid: f2db10cb-a146-412d-8de8-f093253470fd
title: 'Метод ID3DXConstantTable:: Сетматрикстранспосепоинтераррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c78c051ff2d2ab52c9a741fa117a89f66ff450d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713727"
---
# <a name="id3dxconstanttablesetmatrixtransposepointerarray-method"></a><span data-ttu-id="0ebc2-103">Метод ID3DXConstantTable:: Сетматрикстранспосепоинтераррай</span><span class="sxs-lookup"><span data-stu-id="0ebc2-103">ID3DXConstantTable::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="0ebc2-104">Задает массив указателей на перекладываемые матрицы.</span><span class="sxs-lookup"><span data-stu-id="0ebc2-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ebc2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ebc2-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="0ebc2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ebc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ebc2-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ebc2-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ebc2-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0ebc2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0ebc2-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="0ebc2-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="0ebc2-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ebc2-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ebc2-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0ebc2-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0ebc2-112">Уникальный идентификатор массива констант матрицы.</span><span class="sxs-lookup"><span data-stu-id="0ebc2-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="0ebc2-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0ebc2-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ebc2-114">*ппматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ebc2-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ebc2-115">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="0ebc2-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="0ebc2-116">Массив указателей на переликвидированные матрицы.</span><span class="sxs-lookup"><span data-stu-id="0ebc2-116">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="0ebc2-117">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="0ebc2-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ebc2-118">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ebc2-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ebc2-119">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ebc2-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ebc2-120">Число матриц в массиве.</span><span class="sxs-lookup"><span data-stu-id="0ebc2-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ebc2-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ebc2-121">Return value</span></span>

<span data-ttu-id="0ebc2-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ebc2-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ebc2-123">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0ebc2-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0ebc2-124">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="0ebc2-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ebc2-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ebc2-125">Remarks</span></span>

<span data-ttu-id="0ebc2-126">Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.</span><span class="sxs-lookup"><span data-stu-id="0ebc2-126">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ebc2-127">Требования</span><span class="sxs-lookup"><span data-stu-id="0ebc2-127">Requirements</span></span>



| <span data-ttu-id="0ebc2-128">Требование</span><span class="sxs-lookup"><span data-stu-id="0ebc2-128">Requirement</span></span> | <span data-ttu-id="0ebc2-129">Значение</span><span class="sxs-lookup"><span data-stu-id="0ebc2-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebc2-130">Header</span><span class="sxs-lookup"><span data-stu-id="0ebc2-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0ebc2-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ebc2-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0ebc2-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ebc2-132">Library</span></span><br/> | <dl> <span data-ttu-id="0ebc2-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ebc2-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0ebc2-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ebc2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ebc2-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="0ebc2-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
