---
description: Начинает проход в активном методе.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: 'Метод ID3DXEffect:: Бегинпасс (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 56a2648f65c3747f8a98fc0cdbd3ed06cea560b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713721"
---
# <a name="id3dxeffectbeginpass-method"></a><span data-ttu-id="b53b6-103">Метод ID3DXEffect:: Бегинпасс</span><span class="sxs-lookup"><span data-stu-id="b53b6-103">ID3DXEffect::BeginPass method</span></span>

<span data-ttu-id="b53b6-104">Начинает проход в активном методе.</span><span class="sxs-lookup"><span data-stu-id="b53b6-104">Begins a pass, within the active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="b53b6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b53b6-105">Syntax</span></span>


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a><span data-ttu-id="b53b6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b53b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b53b6-107">*Передать* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b53b6-107">*Pass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b53b6-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b53b6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b53b6-109">Отсчитываемый от нуля целочисленный индекс в методе.</span><span class="sxs-lookup"><span data-stu-id="b53b6-109">A zero-based integer index into the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b53b6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b53b6-110">Return value</span></span>

<span data-ttu-id="b53b6-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b53b6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b53b6-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b53b6-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b53b6-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="b53b6-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="b53b6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b53b6-114">Remarks</span></span>

<span data-ttu-id="b53b6-115">Приложение устанавливает один активный проход (в рамках одной активной методики) в системе эффектов, вызывая **ID3DXEffect:: бегинпасс**.</span><span class="sxs-lookup"><span data-stu-id="b53b6-115">An application sets one active pass (within one active technique) in the effect system by calling **ID3DXEffect::BeginPass**.</span></span> <span data-ttu-id="b53b6-116">Приложение сигнализирует об окончании активного прохода, вызвав [**ID3DXEffect:: ендпасс**](id3dxeffect--endpass.md).</span><span class="sxs-lookup"><span data-stu-id="b53b6-116">An application signals the end of the active pass by calling [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md).</span></span> <span data-ttu-id="b53b6-117">**ID3DXEffect:: бегинпасс** и **ID3DXEffect:: ендпасс** должны находиться в соответствующей паре в совпадающей паре [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) и [**ID3DXEffect:: end**](id3dxeffect--end.md) Calls.</span><span class="sxs-lookup"><span data-stu-id="b53b6-117">**ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** must occur in a matching pair, within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and [**ID3DXEffect::End**](id3dxeffect--end.md) calls.</span></span>

<span data-ttu-id="b53b6-118">Если приложение изменяет любое состояние влияния с помощью любого из методов [**Effect:: Setx**](id3dxeffect.md) внутри пары сопоставления **ID3DXEffect:: бегинпасс** / [**ID3DXEffect:: ендпасс**](id3dxeffect--endpass.md) , приложение должно вызвать [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) , чтобы установить обновление устройства с изменением состояния.</span><span class="sxs-lookup"><span data-stu-id="b53b6-118">If the application changes any effect state using any of the [**Effect::Setx**](id3dxeffect.md) methods inside of a **ID3DXEffect::BeginPass**/[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) matching pair, the application must call [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) to set the update the device with the state changes.</span></span> <span data-ttu-id="b53b6-119">Если изменения состояния не происходят в паре **ID3DXEffect:: бегинпасс** и **ID3DXEffect:: Ендпасс** , вызов **ID3DXEffect:: CommitChanges** не требуется.</span><span class="sxs-lookup"><span data-stu-id="b53b6-119">If no state changes occur within a **ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** matching pair, it is not necessary to call **ID3DXEffect::CommitChanges**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b53b6-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b53b6-120">Requirements</span></span>



| <span data-ttu-id="b53b6-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b53b6-121">Requirement</span></span> | <span data-ttu-id="b53b6-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b53b6-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b53b6-123">Header</span><span class="sxs-lookup"><span data-stu-id="b53b6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b53b6-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b53b6-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b53b6-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b53b6-125">Library</span></span><br/> | <dl> <span data-ttu-id="b53b6-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b53b6-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b53b6-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b53b6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b53b6-128">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="b53b6-128">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
