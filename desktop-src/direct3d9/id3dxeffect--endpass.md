---
description: Завершение активного прохода.
ms.assetid: e20b3e0f-db9f-48e8-ab4e-761a5861f3ce
title: 'Метод ID3DXEffect:: Ендпасс (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5cdba799f282e56bbe4565a4792906fd835e5c6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355010"
---
# <a name="id3dxeffectendpass-method"></a><span data-ttu-id="fd03d-103">Метод ID3DXEffect:: Ендпасс</span><span class="sxs-lookup"><span data-stu-id="fd03d-103">ID3DXEffect::EndPass method</span></span>

<span data-ttu-id="fd03d-104">Завершение активного прохода.</span><span class="sxs-lookup"><span data-stu-id="fd03d-104">End an active pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd03d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd03d-105">Syntax</span></span>


```C++
HRESULT EndPass();
```



## <a name="parameters"></a><span data-ttu-id="fd03d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd03d-106">Parameters</span></span>

<span data-ttu-id="fd03d-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fd03d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fd03d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd03d-108">Return value</span></span>

<span data-ttu-id="fd03d-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fd03d-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fd03d-110">Этот метод всегда возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fd03d-110">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd03d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd03d-111">Remarks</span></span>

<span data-ttu-id="fd03d-112">Приложение сообщает об окончании отрисовки активного прохода, вызвав **ID3DXEffect:: ендпасс**.</span><span class="sxs-lookup"><span data-stu-id="fd03d-112">An application signals the end of rendering an active pass by calling **ID3DXEffect::EndPass**.</span></span> <span data-ttu-id="fd03d-113">Каждый **ID3DXEffect:: ендпасс** должен быть частью соответствующей пары вызовов [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md) и **ID3DXEffect:: ендпасс** .</span><span class="sxs-lookup"><span data-stu-id="fd03d-113">Each **ID3DXEffect::EndPass** must be part of a matching pair of [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and **ID3DXEffect::EndPass** calls.</span></span>

<span data-ttu-id="fd03d-114">Все совпадающие пары вызовов [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md) и **ID3DXEffect:: ендпасс** должны находиться в соответствующей паре вызовов [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) и [**ID3DXEffect:: end**](id3dxeffect--end.md) .</span><span class="sxs-lookup"><span data-stu-id="fd03d-114">Each matching pair of [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and **ID3DXEffect::EndPass** calls must be located within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and [**ID3DXEffect::End**](id3dxeffect--end.md) calls.</span></span>

<span data-ttu-id="fd03d-115">Если приложение изменяет любое состояние влияния с помощью любого из методов [**Effect:: Setx**](id3dxeffect.md) внутри пары сопоставления [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md) / **ID3DXEffect:: ендпасс** , приложение должно вызвать [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) перед любым вызовом дравкспримитиве для распространения изменений состояния на устройство перед отрисовкой.</span><span class="sxs-lookup"><span data-stu-id="fd03d-115">If the application changes any effect state using any of the [**Effect::Setx**](id3dxeffect.md) methods inside of a [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md)/**ID3DXEffect::EndPass** matching pair, the application must call [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) before any DrawxPrimitive call to propagate state changes to the device before rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd03d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fd03d-116">Requirements</span></span>



| <span data-ttu-id="fd03d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fd03d-117">Requirement</span></span> | <span data-ttu-id="fd03d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fd03d-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd03d-119">Header</span><span class="sxs-lookup"><span data-stu-id="fd03d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fd03d-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd03d-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="fd03d-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fd03d-121">Library</span></span><br/> | <dl> <span data-ttu-id="fd03d-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd03d-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fd03d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd03d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd03d-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="fd03d-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




