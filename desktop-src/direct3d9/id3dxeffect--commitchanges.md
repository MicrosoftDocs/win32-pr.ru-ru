---
description: Распространите изменения состояния, происходящие внутри активного прохода на устройстве перед отрисовкой.
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: 'Метод ID3DXEffect:: CommitChanges (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CommitChanges
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41516c52b29dfe277cc857e44003de7783282a3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273809"
---
# <a name="id3dxeffectcommitchanges-method"></a><span data-ttu-id="9aa54-103">Метод ID3DXEffect:: CommitChanges</span><span class="sxs-lookup"><span data-stu-id="9aa54-103">ID3DXEffect::CommitChanges method</span></span>

<span data-ttu-id="9aa54-104">Распространите изменения состояния, происходящие внутри активного прохода на устройстве перед отрисовкой.</span><span class="sxs-lookup"><span data-stu-id="9aa54-104">Propagate state changes that occur inside of an active pass to the device before rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa54-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9aa54-105">Syntax</span></span>


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a><span data-ttu-id="9aa54-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9aa54-106">Parameters</span></span>

<span data-ttu-id="9aa54-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9aa54-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9aa54-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9aa54-108">Return value</span></span>

<span data-ttu-id="9aa54-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9aa54-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9aa54-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9aa54-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9aa54-111">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="9aa54-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aa54-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9aa54-112">Remarks</span></span>

<span data-ttu-id="9aa54-113">Если приложение изменяет любое состояние влияния с помощью любого из методов [**ID3DXEffect:: Setx**](id3dxeffect.md) в паре сопоставления [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md) / [**ID3DXEffect:: ендпасс**](id3dxeffect--endpass.md) , приложение должно вызвать **ID3DXEffect:: CommitChanges** перед любым вызовом дравкспримитиве для распространения изменений состояния на устройство перед отрисовкой.</span><span class="sxs-lookup"><span data-stu-id="9aa54-113">If the application changes any effect state using any of the [**ID3DXEffect::Setx**](id3dxeffect.md) methods inside of an [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md)/[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) matching pair, the application must call **ID3DXEffect::CommitChanges** before any DrawxPrimitive call to propagate state changes to the device before rendering.</span></span> <span data-ttu-id="9aa54-114">Если изменения состояния не происходят в паре **ID3DXEffect:: бегинпасс** и **ID3DXEffect:: Ендпасс** , вызов **ID3DXEffect:: CommitChanges** не требуется.</span><span class="sxs-lookup"><span data-stu-id="9aa54-114">If no state changes occur within a **ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** matching pair, it is not necessary to call **ID3DXEffect::CommitChanges**.</span></span>

<span data-ttu-id="9aa54-115">Это несколько отличается для всех общих параметров в клонированном результате.</span><span class="sxs-lookup"><span data-stu-id="9aa54-115">This is slightly different for any shared parameters in a cloned effect.</span></span> <span data-ttu-id="9aa54-116">Если прием активен в клонированном результате (то есть при вызове [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) , но и при вызове [**ID3DXEffect:: end**](id3dxeffect--end.md) не был вызван), **ID3DXEffect:: CommitChanges** обновляет параметры, которые не являются общими, как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="9aa54-116">When a technique is active on a cloned effect (that is, when [**ID3DXEffect::Begin**](id3dxeffect--begin.md) has been called but and [**ID3DXEffect::End**](id3dxeffect--end.md) has not been called), **ID3DXEffect::CommitChanges** updates parameters that are not shared as expected.</span></span> <span data-ttu-id="9aa54-117">Чтобы обновить общий параметр (только для клонированного действия, для которого активен метод), вызовите **ID3DXEffect:: end** , чтобы деактивировать методику, и **ID3DXEffect:: Begin** для повторной активации метода перед вызовом **ID3DXEffect:: CommitChanges**.</span><span class="sxs-lookup"><span data-stu-id="9aa54-117">To update a shared parameter (only for a cloned effect whose technique is active), call **ID3DXEffect::End** to deactivate the technique and **ID3DXEffect::Begin** to reactivate the technique before calling **ID3DXEffect::CommitChanges**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa54-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9aa54-118">Requirements</span></span>



| <span data-ttu-id="9aa54-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9aa54-119">Requirement</span></span> | <span data-ttu-id="9aa54-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9aa54-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa54-121">Header</span><span class="sxs-lookup"><span data-stu-id="9aa54-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9aa54-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aa54-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="9aa54-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9aa54-123">Library</span></span><br/> | <dl> <span data-ttu-id="9aa54-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aa54-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9aa54-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9aa54-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa54-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="9aa54-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




