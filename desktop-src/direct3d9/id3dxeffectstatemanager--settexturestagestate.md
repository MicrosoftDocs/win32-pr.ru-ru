---
description: Функция обратного вызова, которая должна быть реализована пользователем для установки состояния стадии текстуры.
ms.assetid: cc86a483-ccf0-400d-b14d-ab55a3cf4b98
title: 'Метод ID3DXEffectStateManager:: Сеттекстурестажестате (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTextureStageState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 937fd3f2b89dc093d9dceb9441f53d6be2cb06b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674737"
---
# <a name="id3dxeffectstatemanagersettexturestagestate-method"></a><span data-ttu-id="bb7e7-103">Метод ID3DXEffectStateManager:: Сеттекстурестажестате</span><span class="sxs-lookup"><span data-stu-id="bb7e7-103">ID3DXEffectStateManager::SetTextureStageState method</span></span>

<span data-ttu-id="bb7e7-104">Функция обратного вызова, которая должна быть реализована пользователем для установки состояния стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="bb7e7-104">A callback function that must be implemented by a user to set the texture stage state.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb7e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb7e7-105">Syntax</span></span>


```C++
HRESULT SetTextureStageState(
  [in] DWORD                    Stage,
  [in] D3DTEXTURESTAGESTATETYPE Type,
  [in] DWORD                    Value
);
```



## <a name="parameters"></a><span data-ttu-id="bb7e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb7e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb7e7-107">*Этап* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb7e7-107">*Stage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb7e7-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb7e7-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb7e7-109">Этап, которому назначена текстура.</span><span class="sxs-lookup"><span data-stu-id="bb7e7-109">The stage that the texture is assigned to.</span></span> <span data-ttu-id="bb7e7-110">Это значение индекса в [**IDirect3DDevice9:: сеттекстуре**](/windows/desktop/api) или [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="bb7e7-110">This is the index value in [**IDirect3DDevice9::SetTexture**](/windows/desktop/api) or [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span>

</dd> <dt>

<span data-ttu-id="bb7e7-111">*Тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb7e7-111">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb7e7-112">Тип: **[ **D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="bb7e7-112">Type: **[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**</span></span>

<span data-ttu-id="bb7e7-113">Определяет тип операции, которую будет выполнять этап текстуры.</span><span class="sxs-lookup"><span data-stu-id="bb7e7-113">Defines the type of operation that a texture stage will perform.</span></span> <span data-ttu-id="bb7e7-114">См. [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span><span class="sxs-lookup"><span data-stu-id="bb7e7-114">See [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb7e7-115">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb7e7-115">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb7e7-116">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb7e7-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb7e7-117">Может быть либо операцией ([**D3DTEXTUREOP**](./d3dtextureop.md)), либо значением аргумента ([D3DTA](d3dta.md)) в зависимости от того, что выбрано для типа.</span><span class="sxs-lookup"><span data-stu-id="bb7e7-117">Can be either an operation ([**D3DTEXTUREOP**](./d3dtextureop.md)) or an argument value ([D3DTA](d3dta.md)), depending on what is chosen for Type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb7e7-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb7e7-118">Return value</span></span>

<span data-ttu-id="bb7e7-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb7e7-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb7e7-120">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bb7e7-120">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="bb7e7-121">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="bb7e7-121">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="bb7e7-122">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="bb7e7-122">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="bb7e7-123">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="bb7e7-123">The dynamic effect state call (such as [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb7e7-124">Требования</span><span class="sxs-lookup"><span data-stu-id="bb7e7-124">Requirements</span></span>



| <span data-ttu-id="bb7e7-125">Требование</span><span class="sxs-lookup"><span data-stu-id="bb7e7-125">Requirement</span></span> | <span data-ttu-id="bb7e7-126">Значение</span><span class="sxs-lookup"><span data-stu-id="bb7e7-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb7e7-127">Header</span><span class="sxs-lookup"><span data-stu-id="bb7e7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="bb7e7-128"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb7e7-128"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="bb7e7-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bb7e7-129">Library</span></span><br/> | <dl> <span data-ttu-id="bb7e7-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb7e7-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bb7e7-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb7e7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb7e7-132">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="bb7e7-132">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
