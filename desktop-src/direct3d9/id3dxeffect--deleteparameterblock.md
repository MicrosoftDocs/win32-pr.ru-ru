---
description: Удаляет блок параметров.
ms.assetid: 5502dabc-1703-481b-a69d-f6bd8fd01d20
title: 'ID3DXEffect: метод:D Елетепараметерблокк (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.DeleteParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 483b09ebf308b8cdfa14d714bc74786e5fcb1f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713719"
---
# <a name="id3dxeffectdeleteparameterblock-method"></a><span data-ttu-id="defb4-103">ID3DXEffect: метод:D Елетепараметерблокк</span><span class="sxs-lookup"><span data-stu-id="defb4-103">ID3DXEffect::DeleteParameterBlock method</span></span>

<span data-ttu-id="defb4-104">Удаляет блок параметров.</span><span class="sxs-lookup"><span data-stu-id="defb4-104">Delete a parameter block.</span></span>

## <a name="syntax"></a><span data-ttu-id="defb4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="defb4-105">Syntax</span></span>


```C++
HRESULT DeleteParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a><span data-ttu-id="defb4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="defb4-106">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="defb4-107">*хпараметерблокк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="defb4-107">*hParameterBlock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="defb4-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="defb4-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="defb4-109">Маркер блока параметров.</span><span class="sxs-lookup"><span data-stu-id="defb4-109">A handle to the parameter block.</span></span> <span data-ttu-id="defb4-110">Это маркер, возвращаемый [**ID3DXEffect:: ендпараметерблокк**](id3dxeffect--endparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="defb4-110">This is the handle returned by [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="defb4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="defb4-111">Return value</span></span>

<span data-ttu-id="defb4-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="defb4-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="defb4-113">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="defb4-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="defb4-114">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="defb4-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="defb4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="defb4-115">Remarks</span></span>

<span data-ttu-id="defb4-116">Блоки параметров — это блоки состояний эффектов.</span><span class="sxs-lookup"><span data-stu-id="defb4-116">Parameter blocks are blocks of effect states.</span></span> <span data-ttu-id="defb4-117">Используйте блок параметров для записи изменений состояния, чтобы их можно было применить позже с помощью одного вызова API.</span><span class="sxs-lookup"><span data-stu-id="defb4-117">Use a parameter block to record state changes so that they can be applied later on with a single API call.</span></span> <span data-ttu-id="defb4-118">Если больше не требуется, удалите блок параметров, чтобы сократить использование памяти.</span><span class="sxs-lookup"><span data-stu-id="defb4-118">When no longer needed, delete the parameter block to reduce memory usage.</span></span>

## <a name="requirements"></a><span data-ttu-id="defb4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="defb4-119">Requirements</span></span>



| <span data-ttu-id="defb4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="defb4-120">Requirement</span></span> | <span data-ttu-id="defb4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="defb4-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="defb4-122">Header</span><span class="sxs-lookup"><span data-stu-id="defb4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="defb4-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="defb4-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="defb4-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="defb4-124">Library</span></span><br/> | <dl> <span data-ttu-id="defb4-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="defb4-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="defb4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="defb4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="defb4-127">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="defb4-127">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="defb4-128">**ID3DXEffect:: Бегинпараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="defb4-128">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="defb4-129">**ID3DXEffect:: Ендпараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="defb4-129">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> </dl>

 

 




