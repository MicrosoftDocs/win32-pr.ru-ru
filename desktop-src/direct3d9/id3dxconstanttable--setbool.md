---
description: Задает логическое значение.
ms.assetid: 652e5b68-88f3-4b05-959b-38bb530c546a
title: 'Метод ID3DXConstantTable:: Сетбул (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49fb38407aeaaf042d8d606c90e075a1891b9557
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821124"
---
# <a name="id3dxconstanttablesetbool-method"></a><span data-ttu-id="b8ad9-103">Метод ID3DXConstantTable:: Сетбул</span><span class="sxs-lookup"><span data-stu-id="b8ad9-103">ID3DXConstantTable::SetBool method</span></span>

<span data-ttu-id="b8ad9-104">Задает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="b8ad9-104">Sets a Boolean value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8ad9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8ad9-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] BOOL              b
);
```



## <a name="parameters"></a><span data-ttu-id="b8ad9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8ad9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8ad9-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8ad9-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ad9-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b8ad9-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b8ad9-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с таблицей констант.</span><span class="sxs-lookup"><span data-stu-id="b8ad9-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="b8ad9-110">*хконстант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8ad9-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ad9-111">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b8ad9-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b8ad9-112">Уникальный идентификатор константы.</span><span class="sxs-lookup"><span data-stu-id="b8ad9-112">Unique identifier to the constant.</span></span> <span data-ttu-id="b8ad9-113">См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b8ad9-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8ad9-114">*б* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="b8ad9-114">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ad9-115">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8ad9-115">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8ad9-116">.</span><span class="sxs-lookup"><span data-stu-id="b8ad9-116">Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8ad9-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8ad9-117">Return value</span></span>

<span data-ttu-id="b8ad9-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8ad9-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8ad9-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b8ad9-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b8ad9-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="b8ad9-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ad9-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b8ad9-121">Requirements</span></span>



| <span data-ttu-id="b8ad9-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b8ad9-122">Requirement</span></span> | <span data-ttu-id="b8ad9-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b8ad9-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ad9-124">Header</span><span class="sxs-lookup"><span data-stu-id="b8ad9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b8ad9-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8ad9-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b8ad9-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b8ad9-126">Library</span></span><br/> | <dl> <span data-ttu-id="b8ad9-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8ad9-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b8ad9-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8ad9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ad9-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="b8ad9-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
