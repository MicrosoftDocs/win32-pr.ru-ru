---
description: Задает трансобъектную матрицу.
ms.assetid: 1c4d64ce-64bd-47d4-9912-879f4834c0e8
title: 'Метод ID3DXConstantTable:: Сетматрикстранспосе (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa84f9e483be0c6c2ddae37c52ef6df2c43fda90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703810"
---
# <a name="id3dxconstanttablesetmatrixtranspose-method"></a><span data-ttu-id="f94cb-103">Метод ID3DXConstantTable:: Сетматрикстранспосе</span><span class="sxs-lookup"><span data-stu-id="f94cb-103">ID3DXConstantTable::SetMatrixTranspose method</span></span>

<span data-ttu-id="f94cb-104">Задает трансобъектную матрицу.</span><span class="sxs-lookup"><span data-stu-id="f94cb-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f94cb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f94cb-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="f94cb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f94cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f94cb-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f94cb-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f94cb-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f94cb-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f94cb-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="f94cb-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="f94cb-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f94cb-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f94cb-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f94cb-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f94cb-112">Уникальный идентификатор матрицы констант.</span><span class="sxs-lookup"><span data-stu-id="f94cb-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="f94cb-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f94cb-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="f94cb-114">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f94cb-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f94cb-115">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f94cb-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f94cb-116">Указатель на переустановленную матрицу.</span><span class="sxs-lookup"><span data-stu-id="f94cb-116">Pointer to a transposed matrix.</span></span> <span data-ttu-id="f94cb-117">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="f94cb-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f94cb-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f94cb-118">Return value</span></span>

<span data-ttu-id="f94cb-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f94cb-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f94cb-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f94cb-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f94cb-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="f94cb-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f94cb-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f94cb-122">Requirements</span></span>



| <span data-ttu-id="f94cb-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f94cb-123">Requirement</span></span> | <span data-ttu-id="f94cb-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f94cb-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f94cb-125">Header</span><span class="sxs-lookup"><span data-stu-id="f94cb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f94cb-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f94cb-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f94cb-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f94cb-127">Library</span></span><br/> | <dl> <span data-ttu-id="f94cb-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f94cb-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f94cb-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f94cb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f94cb-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="f94cb-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
