---
description: Применить значения в блоке состояния к текущему состоянию системы.
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: 'Метод ID3DXEffect:: Апплипараметерблокк (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ApplyParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 12af672b929822180c4dba681ca333692a9174ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713724"
---
# <a name="id3dxeffectapplyparameterblock-method"></a><span data-ttu-id="182f6-103">Метод ID3DXEffect:: Апплипараметерблокк</span><span class="sxs-lookup"><span data-stu-id="182f6-103">ID3DXEffect::ApplyParameterBlock method</span></span>

<span data-ttu-id="182f6-104">Применить значения в блоке состояния к текущему состоянию системы.</span><span class="sxs-lookup"><span data-stu-id="182f6-104">Apply the values in a state block to the current effect system state.</span></span>

## <a name="syntax"></a><span data-ttu-id="182f6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="182f6-105">Syntax</span></span>


```C++
HRESULT ApplyParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a><span data-ttu-id="182f6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="182f6-106">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="182f6-107">*хпараметерблокк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="182f6-107">*hParameterBlock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182f6-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="182f6-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="182f6-109">Маркер блока параметров.</span><span class="sxs-lookup"><span data-stu-id="182f6-109">A handle to the parameter block.</span></span> <span data-ttu-id="182f6-110">Это маркер, возвращаемый [**ID3DXEffect:: ендпараметерблокк**](id3dxeffect--endparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="182f6-110">This is the handle returned by [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="182f6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="182f6-111">Return value</span></span>

<span data-ttu-id="182f6-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="182f6-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="182f6-113">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="182f6-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="182f6-114">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="182f6-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="182f6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="182f6-115">Remarks</span></span>

<span data-ttu-id="182f6-116">Изменения состояния параметров эффектов захвата в блоке параметров путем вызова Бегинпараметерблокк; останавливает запись изменений состояния путем вызова Ендпараметерблокк.</span><span class="sxs-lookup"><span data-stu-id="182f6-116">Capture effect parameter state changes in a parameter block by calling BeginParameterBlock; stop capturing state changes by calling EndParameterBlock.</span></span> <span data-ttu-id="182f6-117">Эти изменения состояния включают любые изменения параметров эффектов, происходящие внутри метода (в том числе за пределами прохода).</span><span class="sxs-lookup"><span data-stu-id="182f6-117">These state changes include any effect parameter changes that occur inside of a technique (including those outside of a pass).</span></span> <span data-ttu-id="182f6-118">Когда вы завершите работу с блоком параметров, вызовите Делетепараметерблокк для восстановления памяти.</span><span class="sxs-lookup"><span data-stu-id="182f6-118">Once you are done with the parameter block, call DeleteParameterBlock to recover memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="182f6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="182f6-119">Requirements</span></span>



| <span data-ttu-id="182f6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="182f6-120">Requirement</span></span> | <span data-ttu-id="182f6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="182f6-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="182f6-122">Header</span><span class="sxs-lookup"><span data-stu-id="182f6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="182f6-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="182f6-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="182f6-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="182f6-124">Library</span></span><br/> | <dl> <span data-ttu-id="182f6-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="182f6-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="182f6-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="182f6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="182f6-127">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="182f6-127">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="182f6-128">**ID3DXEffect:: Бегинпараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="182f6-128">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="182f6-129">**ID3DXEffect:: Ендпараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="182f6-129">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> <dt>

[<span data-ttu-id="182f6-130">**ID3DXEffect::D Елетепараметерблокк**</span><span class="sxs-lookup"><span data-stu-id="182f6-130">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




