---
description: Функция обратного вызова, которая должна быть реализована пользователем для установки кода ФВФ.
ms.assetid: 701a4333-a71e-4d84-a06c-1c86312ee4ff
title: 'Метод ID3DXEffectStateManager:: Сетфвф (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetFVF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a68ab07e4f486a8df80ecde5844739a6a010c2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694210"
---
# <a name="id3dxeffectstatemanagersetfvf-method"></a><span data-ttu-id="d543e-103">Метод ID3DXEffectStateManager:: Сетфвф</span><span class="sxs-lookup"><span data-stu-id="d543e-103">ID3DXEffectStateManager::SetFVF method</span></span>

<span data-ttu-id="d543e-104">Функция обратного вызова, которая должна быть реализована пользователем для установки кода ФВФ.</span><span class="sxs-lookup"><span data-stu-id="d543e-104">A callback function that must be implemented by a user to set a FVF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d543e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d543e-105">Syntax</span></span>


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="d543e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d543e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d543e-107">*Фвф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d543e-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d543e-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d543e-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d543e-109">Константа ФВФ, определяющая способ интерпретации данных вершин.</span><span class="sxs-lookup"><span data-stu-id="d543e-109">The FVF constant, that determines how to interpret vertex data.</span></span> <span data-ttu-id="d543e-110">См. [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="d543e-110">See [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d543e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d543e-111">Return value</span></span>

<span data-ttu-id="d543e-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d543e-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d543e-113">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d543e-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="d543e-114">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="d543e-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="d543e-115">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="d543e-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="d543e-116">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетфвф**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d543e-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="d543e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d543e-117">Requirements</span></span>



| <span data-ttu-id="d543e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d543e-118">Requirement</span></span> | <span data-ttu-id="d543e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d543e-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d543e-120">Header</span><span class="sxs-lookup"><span data-stu-id="d543e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d543e-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d543e-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="d543e-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d543e-122">Library</span></span><br/> | <dl> <span data-ttu-id="d543e-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d543e-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d543e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d543e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d543e-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="d543e-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
