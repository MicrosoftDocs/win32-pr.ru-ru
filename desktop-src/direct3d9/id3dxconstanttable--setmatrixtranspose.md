---
description: 'Метод ID3DXConstantTable:: Сетматрикстранспосе — задает перекладываемую матрицу.'
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
ms.openlocfilehash: 06cc989a14da6f2fe84d30f7f5d7d9fc35acd3bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115062"
---
# <a name="id3dxconstanttablesetmatrixtranspose-method"></a><span data-ttu-id="bab78-103">Метод ID3DXConstantTable:: Сетматрикстранспосе</span><span class="sxs-lookup"><span data-stu-id="bab78-103">ID3DXConstantTable::SetMatrixTranspose method</span></span>

<span data-ttu-id="bab78-104">Задает трансобъектную матрицу.</span><span class="sxs-lookup"><span data-stu-id="bab78-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab78-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bab78-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="bab78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bab78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bab78-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bab78-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab78-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="bab78-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="bab78-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="bab78-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="bab78-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bab78-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab78-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bab78-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bab78-112">Уникальный идентификатор матрицы констант.</span><span class="sxs-lookup"><span data-stu-id="bab78-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="bab78-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="bab78-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab78-114">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bab78-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bab78-115">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bab78-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bab78-116">Указатель на переустановленную матрицу.</span><span class="sxs-lookup"><span data-stu-id="bab78-116">Pointer to a transposed matrix.</span></span> <span data-ttu-id="bab78-117">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="bab78-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bab78-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bab78-118">Return value</span></span>

<span data-ttu-id="bab78-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bab78-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bab78-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bab78-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bab78-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="bab78-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bab78-122">Требования</span><span class="sxs-lookup"><span data-stu-id="bab78-122">Requirements</span></span>



| <span data-ttu-id="bab78-123">Требование</span><span class="sxs-lookup"><span data-stu-id="bab78-123">Requirement</span></span> | <span data-ttu-id="bab78-124">Значение</span><span class="sxs-lookup"><span data-stu-id="bab78-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bab78-125">Header</span><span class="sxs-lookup"><span data-stu-id="bab78-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bab78-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="bab78-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bab78-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bab78-127">Library</span></span><br/> | <dl> <span data-ttu-id="bab78-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bab78-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bab78-129">См. также</span><span class="sxs-lookup"><span data-stu-id="bab78-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab78-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="bab78-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
