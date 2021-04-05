---
description: Начать запись изменений состояния в блоке параметров.
ms.assetid: cdf6f572-1a21-4c1d-a113-13b48bacd060
title: 'Метод ID3DXEffect:: Бегинпараметерблокк (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 60a43304c8e0e3d64ac6469c1c075c57b5411e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081874"
---
# <a name="id3dxeffectbeginparameterblock-method"></a><span data-ttu-id="2d046-103">Метод ID3DXEffect:: Бегинпараметерблокк</span><span class="sxs-lookup"><span data-stu-id="2d046-103">ID3DXEffect::BeginParameterBlock method</span></span>

<span data-ttu-id="2d046-104">Начать запись изменений состояния в блоке параметров.</span><span class="sxs-lookup"><span data-stu-id="2d046-104">Start capturing state changes in a parameter block.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d046-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d046-105">Syntax</span></span>


```C++
HRESULT BeginParameterBlock();
```



## <a name="parameters"></a><span data-ttu-id="2d046-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d046-106">Parameters</span></span>

<span data-ttu-id="2d046-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2d046-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2d046-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d046-108">Return value</span></span>

<span data-ttu-id="2d046-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d046-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d046-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2d046-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2d046-111">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="2d046-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d046-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d046-112">Remarks</span></span>

<span data-ttu-id="2d046-113">Изменения состояния параметров эффектов захвата до вызова Ендпараметерблокк.</span><span class="sxs-lookup"><span data-stu-id="2d046-113">Capture effect parameter state changes until EndParameterBlock is called.</span></span> <span data-ttu-id="2d046-114">Параметры эффектов включают любые изменения состояния, находящиеся за пределами прохода.</span><span class="sxs-lookup"><span data-stu-id="2d046-114">Effect parameters include any state changes outside of a pass.</span></span> <span data-ttu-id="2d046-115">Удалите блоки параметров, если они больше не нужны, вызвав Делетепараметерблокк.</span><span class="sxs-lookup"><span data-stu-id="2d046-115">Delete parameter blocks if they are no longer needed by calling DeleteParameterBlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d046-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2d046-116">Requirements</span></span>



| <span data-ttu-id="2d046-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2d046-117">Requirement</span></span> | <span data-ttu-id="2d046-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2d046-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d046-119">Header</span><span class="sxs-lookup"><span data-stu-id="2d046-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2d046-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d046-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2d046-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2d046-121">Library</span></span><br/> | <dl> <span data-ttu-id="2d046-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d046-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2d046-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d046-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d046-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="2d046-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="2d046-125">**ID3DXEffect:: Ендпараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="2d046-125">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> <dt>

[<span data-ttu-id="2d046-126">**ID3DXEffect:: Апплипараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="2d046-126">**ID3DXEffect::ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[<span data-ttu-id="2d046-127">**ID3DXEffect::D Елетепараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="2d046-127">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




