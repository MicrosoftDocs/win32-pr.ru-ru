---
description: Задает вектор 4D.
ms.assetid: d5849a8b-b372-4ad0-8773-8c9c4bac3799
title: 'Метод ID3DXConstantTable:: Сетвектор (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ace1e7b12b67173eb5b9d9a5fc5e56a8b360f2b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703808"
---
# <a name="id3dxconstanttablesetvector-method"></a><span data-ttu-id="1e215-103">Метод ID3DXConstantTable:: Сетвектор</span><span class="sxs-lookup"><span data-stu-id="1e215-103">ID3DXConstantTable::SetVector method</span></span>

<span data-ttu-id="1e215-104">Задает вектор 4D.</span><span class="sxs-lookup"><span data-stu-id="1e215-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e215-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e215-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="1e215-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e215-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e215-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e215-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e215-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1e215-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1e215-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="1e215-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="1e215-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e215-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e215-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1e215-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1e215-112">Уникальный идентификатор константы Vector.</span><span class="sxs-lookup"><span data-stu-id="1e215-112">Unique identifier to the vector constant.</span></span> <span data-ttu-id="1e215-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1e215-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e215-114">*пвектор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e215-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e215-115">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1e215-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1e215-116">Указатель на вектор 4D.</span><span class="sxs-lookup"><span data-stu-id="1e215-116">Pointer to a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e215-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e215-117">Return value</span></span>

<span data-ttu-id="1e215-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1e215-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1e215-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1e215-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1e215-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="1e215-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e215-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1e215-121">Requirements</span></span>



| <span data-ttu-id="1e215-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1e215-122">Requirement</span></span> | <span data-ttu-id="1e215-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1e215-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e215-124">Header</span><span class="sxs-lookup"><span data-stu-id="1e215-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1e215-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e215-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1e215-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1e215-126">Library</span></span><br/> | <dl> <span data-ttu-id="1e215-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e215-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1e215-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e215-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e215-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="1e215-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
