---
description: Функция обратного вызова, которая должна быть реализована пользователем для задания шейдера пикселей.
ms.assetid: 4124eff2-1d88-429c-b7ed-8d87155b5ddc
title: 'Метод ID3DXEffectStateManager:: Сетпикселшадер (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 71a16bc267df95ed7efc1e0f74871b131e34ebe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547999"
---
# <a name="id3dxeffectstatemanagersetpixelshader-method"></a><span data-ttu-id="179f6-103">Метод ID3DXEffectStateManager:: Сетпикселшадер</span><span class="sxs-lookup"><span data-stu-id="179f6-103">ID3DXEffectStateManager::SetPixelShader method</span></span>

<span data-ttu-id="179f6-104">Функция обратного вызова, которая должна быть реализована пользователем для задания шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="179f6-104">A callback function that must be implemented by a user to set a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="179f6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="179f6-105">Syntax</span></span>


```C++
HRESULT SetPixelShader(
  [in] LPDIRECT3DPIXELSHADER9 pShader
);
```



## <a name="parameters"></a><span data-ttu-id="179f6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="179f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="179f6-107">*пшадер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="179f6-107">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="179f6-108">Тип: **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)**</span><span class="sxs-lookup"><span data-stu-id="179f6-108">Type: **[**LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)**</span></span>

<span data-ttu-id="179f6-109">Указатель на объект шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="179f6-109">A pointer to a pixel shader object.</span></span> <span data-ttu-id="179f6-110">См. [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9).</span><span class="sxs-lookup"><span data-stu-id="179f6-110">See [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="179f6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="179f6-111">Return value</span></span>

<span data-ttu-id="179f6-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="179f6-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="179f6-113">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="179f6-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="179f6-114">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="179f6-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="179f6-115">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="179f6-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="179f6-116">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетпикселшадер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="179f6-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="179f6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="179f6-117">Requirements</span></span>



| <span data-ttu-id="179f6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="179f6-118">Requirement</span></span> | <span data-ttu-id="179f6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="179f6-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="179f6-120">Header</span><span class="sxs-lookup"><span data-stu-id="179f6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="179f6-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="179f6-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="179f6-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="179f6-122">Library</span></span><br/> | <dl> <span data-ttu-id="179f6-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="179f6-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="179f6-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="179f6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="179f6-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="179f6-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
