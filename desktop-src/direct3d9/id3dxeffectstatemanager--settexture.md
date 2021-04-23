---
description: Функция обратного вызова, которая должна быть реализована пользователем для установки текстуры.
ms.assetid: 971802f4-ea7a-4906-83b8-0cd83111716e
title: 'Метод ID3DXEffectStateManager:: Сеттекстуре (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b395c19b65bb39b8328da24f727292f7dbe2a0f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547991"
---
# <a name="id3dxeffectstatemanagersettexture-method"></a><span data-ttu-id="a4b50-103">Метод ID3DXEffectStateManager:: Сеттекстуре</span><span class="sxs-lookup"><span data-stu-id="a4b50-103">ID3DXEffectStateManager::SetTexture method</span></span>

<span data-ttu-id="a4b50-104">Функция обратного вызова, которая должна быть реализована пользователем для установки текстуры.</span><span class="sxs-lookup"><span data-stu-id="a4b50-104">A callback function that must be implemented by a user to set a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b50-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4b50-105">Syntax</span></span>


```C++
HRESULT SetTexture(
  [in] DWORD                  Stage,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="a4b50-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4b50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4b50-107">*Этап* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4b50-107">*Stage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b50-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4b50-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a4b50-109">Этап, которому назначена текстура.</span><span class="sxs-lookup"><span data-stu-id="a4b50-109">The stage to which the texture is assigned.</span></span> <span data-ttu-id="a4b50-110">Это значение индекса в [**IDirect3DDevice9:: сеттекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) или [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="a4b50-110">This is the index value in [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) or [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span>

</dd> <dt>

<span data-ttu-id="a4b50-111">*птекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4b50-111">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b50-112">Тип: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="a4b50-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="a4b50-113">Указатель на объект текстуры.</span><span class="sxs-lookup"><span data-stu-id="a4b50-113">A pointer to the texture object.</span></span> <span data-ttu-id="a4b50-114">Это может быть любой из типов текстур Direct3D (куб, том и т. д.).</span><span class="sxs-lookup"><span data-stu-id="a4b50-114">This can be any of the Direct3D texture types (cube, volume, etc.).</span></span> <span data-ttu-id="a4b50-115">См. [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="a4b50-115">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4b50-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4b50-116">Return value</span></span>

<span data-ttu-id="a4b50-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a4b50-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a4b50-118">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a4b50-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="a4b50-119">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="a4b50-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="a4b50-120">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="a4b50-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="a4b50-121">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сеттекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a4b50-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b50-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a4b50-122">Requirements</span></span>



| <span data-ttu-id="a4b50-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a4b50-123">Requirement</span></span> | <span data-ttu-id="a4b50-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a4b50-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b50-125">Header</span><span class="sxs-lookup"><span data-stu-id="a4b50-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a4b50-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4b50-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a4b50-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a4b50-127">Library</span></span><br/> | <dl> <span data-ttu-id="a4b50-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4b50-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a4b50-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4b50-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b50-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="a4b50-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
