---
description: Функция обратного вызова, которая должна быть реализована пользователем для включения или отключения освещения.
ms.assetid: 11522ca3-8a2f-4767-a6e6-4186cb4f3115
title: 'Метод ID3DXEffectStateManager:: осветлить (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.LightEnable
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d065540eb036b26cdd19791dc393d32c5b45e3ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273862"
---
# <a name="id3dxeffectstatemanagerlightenable-method"></a><span data-ttu-id="ddd91-103">ID3DXEffectStateManager:: досветлющий метод</span><span class="sxs-lookup"><span data-stu-id="ddd91-103">ID3DXEffectStateManager::LightEnable method</span></span>

<span data-ttu-id="ddd91-104">Функция обратного вызова, которая должна быть реализована пользователем для включения или отключения освещения.</span><span class="sxs-lookup"><span data-stu-id="ddd91-104">A callback function that must be implemented by a user to enable/disable a light.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddd91-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ddd91-105">Syntax</span></span>


```C++
HRESULT LightEnable(
  [in] DWORD Index,
  [in] BOOL  Enable
);
```



## <a name="parameters"></a><span data-ttu-id="ddd91-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ddd91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddd91-107">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddd91-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddd91-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ddd91-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ddd91-109">Отсчитываемый от нуля индекс источника освещения.</span><span class="sxs-lookup"><span data-stu-id="ddd91-109">The zero-based index of the light.</span></span> <span data-ttu-id="ddd91-110">Это тот же индекс в [**IDirect3DDevice9:: сетлигхт**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span><span class="sxs-lookup"><span data-stu-id="ddd91-110">This is the same index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span></span>

</dd> <dt>

<span data-ttu-id="ddd91-111">*Включить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddd91-111">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddd91-112">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ddd91-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ddd91-113">Значение true, чтобы включить освещение; в противном случае — false.</span><span class="sxs-lookup"><span data-stu-id="ddd91-113">True to enable the light, false otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddd91-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ddd91-114">Return value</span></span>

<span data-ttu-id="ddd91-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ddd91-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ddd91-116">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ddd91-116">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="ddd91-117">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="ddd91-117">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="ddd91-118">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="ddd91-118">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="ddd91-119">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: осветлить**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ddd91-119">The dynamic effect state call (such as [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddd91-120">Требования</span><span class="sxs-lookup"><span data-stu-id="ddd91-120">Requirements</span></span>



| <span data-ttu-id="ddd91-121">Требование</span><span class="sxs-lookup"><span data-stu-id="ddd91-121">Requirement</span></span> | <span data-ttu-id="ddd91-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ddd91-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddd91-123">Header</span><span class="sxs-lookup"><span data-stu-id="ddd91-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ddd91-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddd91-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="ddd91-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ddd91-125">Library</span></span><br/> | <dl> <span data-ttu-id="ddd91-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddd91-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ddd91-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddd91-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddd91-128">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="ddd91-128">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
