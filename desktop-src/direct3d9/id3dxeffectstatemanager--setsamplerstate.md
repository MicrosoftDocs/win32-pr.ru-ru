---
description: Функция обратного вызова, которая должна быть реализована пользователем для установки образца.
ms.assetid: 1e19e8cd-341d-4372-9182-8b3c82155407
title: 'Метод ID3DXEffectStateManager:: Сетсамплерстате (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetSamplerState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bba12db8dbc1902adc5c64b4cc1726e081dfea70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355180"
---
# <a name="id3dxeffectstatemanagersetsamplerstate-method"></a><span data-ttu-id="f60fb-103">Метод ID3DXEffectStateManager:: Сетсамплерстате</span><span class="sxs-lookup"><span data-stu-id="f60fb-103">ID3DXEffectStateManager::SetSamplerState method</span></span>

<span data-ttu-id="f60fb-104">Функция обратного вызова, которая должна быть реализована пользователем для установки образца.</span><span class="sxs-lookup"><span data-stu-id="f60fb-104">A callback function that must be implemented by a user to set a sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="f60fb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f60fb-105">Syntax</span></span>


```C++
HRESULT SetSamplerState(
  [in] DWORD               Sampler,
  [in] D3DSAMPLERSTATETYPE Type,
  [in] DWORD               Value
);
```



## <a name="parameters"></a><span data-ttu-id="f60fb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f60fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f60fb-107">*Образец* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f60fb-107">*Sampler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f60fb-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f60fb-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f60fb-109">Номер образца для отсчета от нуля.</span><span class="sxs-lookup"><span data-stu-id="f60fb-109">The zero-based sampler number.</span></span>

</dd> <dt>

<span data-ttu-id="f60fb-110">*Тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f60fb-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f60fb-111">Тип: **[ **D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="f60fb-111">Type: **[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**</span></span>

<span data-ttu-id="f60fb-112">Определяет состояние образца, которое может определять фильтрацию, адресацию или цвет границы.</span><span class="sxs-lookup"><span data-stu-id="f60fb-112">Identifies sampler state, which can specify the filtering, addressing, or the border color.</span></span> <span data-ttu-id="f60fb-113">См. [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="f60fb-113">See [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="f60fb-114">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f60fb-114">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f60fb-115">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f60fb-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f60fb-116">Значение из одного из типов состояния выборки в поле Тип.</span><span class="sxs-lookup"><span data-stu-id="f60fb-116">A value from one of the sampler state types in Type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f60fb-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f60fb-117">Return value</span></span>

<span data-ttu-id="f60fb-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f60fb-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f60fb-119">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f60fb-119">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="f60fb-120">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="f60fb-120">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="f60fb-121">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="f60fb-121">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="f60fb-122">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="f60fb-122">The dynamic effect state call (such as [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="f60fb-123">Требования</span><span class="sxs-lookup"><span data-stu-id="f60fb-123">Requirements</span></span>



| <span data-ttu-id="f60fb-124">Требование</span><span class="sxs-lookup"><span data-stu-id="f60fb-124">Requirement</span></span> | <span data-ttu-id="f60fb-125">Значение</span><span class="sxs-lookup"><span data-stu-id="f60fb-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f60fb-126">Header</span><span class="sxs-lookup"><span data-stu-id="f60fb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f60fb-127"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f60fb-127"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f60fb-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f60fb-128">Library</span></span><br/> | <dl> <span data-ttu-id="f60fb-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f60fb-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f60fb-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f60fb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f60fb-131">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="f60fb-131">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
