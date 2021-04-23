---
description: Задает матрицу нонтранспосед.
ms.assetid: 30369e34-6e9d-4480-a142-e38f46fd38b0
title: 'Метод ID3DXConstantTable:: Сетматрикс (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ae227663a61087fae309d1954b8f0dc438f6df2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694184"
---
# <a name="id3dxconstanttablesetmatrix-method"></a><span data-ttu-id="c57ee-103">Метод ID3DXConstantTable:: Сетматрикс</span><span class="sxs-lookup"><span data-stu-id="c57ee-103">ID3DXConstantTable::SetMatrix method</span></span>

<span data-ttu-id="c57ee-104">Задает матрицу нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="c57ee-104">Sets a nontransposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c57ee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c57ee-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="c57ee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c57ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c57ee-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c57ee-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c57ee-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c57ee-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c57ee-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="c57ee-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="c57ee-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c57ee-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c57ee-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c57ee-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c57ee-112">Уникальный идентификатор матрицы констант.</span><span class="sxs-lookup"><span data-stu-id="c57ee-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="c57ee-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c57ee-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c57ee-114">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c57ee-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c57ee-115">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c57ee-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c57ee-116">Указатель на матрицу нонтранспосед.</span><span class="sxs-lookup"><span data-stu-id="c57ee-116">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="c57ee-117">См. [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="c57ee-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c57ee-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c57ee-118">Return value</span></span>

<span data-ttu-id="c57ee-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c57ee-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c57ee-120">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c57ee-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c57ee-121">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="c57ee-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c57ee-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c57ee-122">Requirements</span></span>



| <span data-ttu-id="c57ee-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c57ee-123">Requirement</span></span> | <span data-ttu-id="c57ee-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c57ee-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c57ee-125">Header</span><span class="sxs-lookup"><span data-stu-id="c57ee-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c57ee-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c57ee-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c57ee-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c57ee-127">Library</span></span><br/> | <dl> <span data-ttu-id="c57ee-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c57ee-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c57ee-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c57ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c57ee-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="c57ee-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
