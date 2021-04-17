---
description: Функция обратного вызова, которая должна быть реализована пользователем для установки освещения.
ms.assetid: 3b9b2cbd-79f5-4ea4-a47b-da23b091adfd
title: 'Метод ID3DXEffectStateManager:: Сетлигхт (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetLight
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1306283b098922706f39abc7ffe2514d2fba0e5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694209"
---
# <a name="id3dxeffectstatemanagersetlight-method"></a><span data-ttu-id="44503-103">Метод ID3DXEffectStateManager:: Сетлигхт</span><span class="sxs-lookup"><span data-stu-id="44503-103">ID3DXEffectStateManager::SetLight method</span></span>

<span data-ttu-id="44503-104">Функция обратного вызова, которая должна быть реализована пользователем для установки освещения.</span><span class="sxs-lookup"><span data-stu-id="44503-104">A callback function that must be implemented by a user to set a light.</span></span>

## <a name="syntax"></a><span data-ttu-id="44503-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44503-105">Syntax</span></span>


```C++
HRESULT SetLight(
  [in]       DWORD     Index,
  [in] const D3DLight9 *pLight
);
```



## <a name="parameters"></a><span data-ttu-id="44503-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="44503-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44503-107">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44503-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44503-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44503-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44503-109">Отсчитываемый от нуля индекс источника освещения.</span><span class="sxs-lookup"><span data-stu-id="44503-109">The zero-based index of the light.</span></span> <span data-ttu-id="44503-110">Это тот же индекс в [**IDirect3DDevice9:: сетлигхт**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span><span class="sxs-lookup"><span data-stu-id="44503-110">This is the same index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span></span>

</dd> <dt>

<span data-ttu-id="44503-111">*плигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44503-111">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44503-112">Тип: **const [**D3DLight9**](d3dlight9.md) \***</span><span class="sxs-lookup"><span data-stu-id="44503-112">Type: **const [**D3DLight9**](d3dlight9.md)\***</span></span>

<span data-ttu-id="44503-113">Объект light.</span><span class="sxs-lookup"><span data-stu-id="44503-113">The light object.</span></span> <span data-ttu-id="44503-114">См. [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="44503-114">See [**D3DLIGHT9**](d3dlight9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44503-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44503-115">Return value</span></span>

<span data-ttu-id="44503-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="44503-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="44503-117">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="44503-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="44503-118">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="44503-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="44503-119">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="44503-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="44503-120">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетлигхт**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="44503-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="44503-121">Требования</span><span class="sxs-lookup"><span data-stu-id="44503-121">Requirements</span></span>



| <span data-ttu-id="44503-122">Требование</span><span class="sxs-lookup"><span data-stu-id="44503-122">Requirement</span></span> | <span data-ttu-id="44503-123">Значение</span><span class="sxs-lookup"><span data-stu-id="44503-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44503-124">Header</span><span class="sxs-lookup"><span data-stu-id="44503-124">Header</span></span><br/>  | <dl> <span data-ttu-id="44503-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="44503-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="44503-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="44503-126">Library</span></span><br/> | <dl> <span data-ttu-id="44503-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44503-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="44503-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44503-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44503-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="44503-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
