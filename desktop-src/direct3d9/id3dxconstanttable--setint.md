---
description: Задает целочисленное значение.
ms.assetid: b57d30b5-c2b5-469e-a267-24e6e712d645
title: 'Метод ID3DXConstantTable:: SetInt (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetInt
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a0aa0a213f9f4704a5d557db66aaf360f8baa727
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713732"
---
# <a name="id3dxconstanttablesetint-method"></a><span data-ttu-id="fb248-103">Метод ID3DXConstantTable:: SetInt</span><span class="sxs-lookup"><span data-stu-id="fb248-103">ID3DXConstantTable::SetInt method</span></span>

<span data-ttu-id="fb248-104">Задает целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="fb248-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb248-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb248-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] INT               n
);
```



## <a name="parameters"></a><span data-ttu-id="fb248-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb248-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb248-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb248-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb248-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="fb248-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="fb248-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="fb248-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="fb248-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb248-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb248-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fb248-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fb248-112">Уникальный идентификатор константы.</span><span class="sxs-lookup"><span data-stu-id="fb248-112">Unique identifier to the constant.</span></span> <span data-ttu-id="fb248-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fb248-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb248-114">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="fb248-114">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb248-115">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb248-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb248-116">Целое число.</span><span class="sxs-lookup"><span data-stu-id="fb248-116">Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb248-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb248-117">Return value</span></span>

<span data-ttu-id="fb248-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb248-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb248-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fb248-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fb248-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="fb248-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb248-121">Требования</span><span class="sxs-lookup"><span data-stu-id="fb248-121">Requirements</span></span>



| <span data-ttu-id="fb248-122">Требование</span><span class="sxs-lookup"><span data-stu-id="fb248-122">Requirement</span></span> | <span data-ttu-id="fb248-123">Значение</span><span class="sxs-lookup"><span data-stu-id="fb248-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb248-124">Header</span><span class="sxs-lookup"><span data-stu-id="fb248-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fb248-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb248-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fb248-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fb248-126">Library</span></span><br/> | <dl> <span data-ttu-id="fb248-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb248-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fb248-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb248-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb248-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="fb248-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
