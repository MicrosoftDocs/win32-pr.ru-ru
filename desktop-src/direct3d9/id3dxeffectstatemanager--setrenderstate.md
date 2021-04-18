---
description: Функция обратного вызова, которая должна быть реализована пользователем для установки состояния отрисовки.
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: 'Метод ID3DXEffectStateManager:: Сетрендерстате (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 111ab8ff379d5b095500101674fc45b6a2b31bc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713782"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a><span data-ttu-id="c119a-103">Метод ID3DXEffectStateManager:: Сетрендерстате</span><span class="sxs-lookup"><span data-stu-id="c119a-103">ID3DXEffectStateManager::SetRenderState method</span></span>

<span data-ttu-id="c119a-104">Функция обратного вызова, которая должна быть реализована пользователем для установки состояния отрисовки.</span><span class="sxs-lookup"><span data-stu-id="c119a-104">A callback function that must be implemented by a user to set render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="c119a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c119a-105">Syntax</span></span>


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a><span data-ttu-id="c119a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c119a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c119a-107">*Состояние* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c119a-107">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c119a-108">Тип: **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="c119a-108">Type: **[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**</span></span>

<span data-ttu-id="c119a-109">Заданное состояние отрисовки.</span><span class="sxs-lookup"><span data-stu-id="c119a-109">The render state to set.</span></span> [<span data-ttu-id="c119a-110">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="c119a-110">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)

</dd> <dt>

<span data-ttu-id="c119a-111">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c119a-111">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c119a-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c119a-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c119a-113">Значение состояния отрисовки.</span><span class="sxs-lookup"><span data-stu-id="c119a-113">The render state value.</span></span> <span data-ttu-id="c119a-114">См. раздел [состояния эффектов (Direct3D 9)](effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="c119a-114">See [Effect States (Direct3D 9)](effect-states.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c119a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c119a-115">Return value</span></span>

<span data-ttu-id="c119a-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c119a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c119a-117">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c119a-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="c119a-118">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="c119a-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="c119a-119">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="c119a-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="c119a-120">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c119a-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="c119a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c119a-121">Requirements</span></span>



| <span data-ttu-id="c119a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c119a-122">Requirement</span></span> | <span data-ttu-id="c119a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c119a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c119a-124">Header</span><span class="sxs-lookup"><span data-stu-id="c119a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c119a-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c119a-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c119a-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c119a-126">Library</span></span><br/> | <dl> <span data-ttu-id="c119a-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c119a-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c119a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c119a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c119a-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="c119a-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
