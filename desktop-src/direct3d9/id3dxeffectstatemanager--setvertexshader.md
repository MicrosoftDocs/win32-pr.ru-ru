---
description: Функция обратного вызова, которая должна быть реализована пользователем для задания шейдера вершин.
ms.assetid: 8f3d3be3-c073-441d-a318-6d2cd5e7aca5
title: 'Метод ID3DXEffectStateManager:: Сетвертексшадер (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9fd25158f2aa6ab0a22d6226e8e709c3b498b0e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914776"
---
# <a name="id3dxeffectstatemanagersetvertexshader-method"></a><span data-ttu-id="b488f-103">Метод ID3DXEffectStateManager:: Сетвертексшадер</span><span class="sxs-lookup"><span data-stu-id="b488f-103">ID3DXEffectStateManager::SetVertexShader method</span></span>

<span data-ttu-id="b488f-104">Функция обратного вызова, которая должна быть реализована пользователем для задания шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="b488f-104">A callback function that must be implemented by a user to set a vertex shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="b488f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b488f-105">Syntax</span></span>


```C++
HRESULT SetVertexShader(
  [in] LPDIRECT3DVERTEXSHADER9 pShader
);
```



## <a name="parameters"></a><span data-ttu-id="b488f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b488f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b488f-107">*пшадер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b488f-107">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b488f-108">Тип: **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**</span><span class="sxs-lookup"><span data-stu-id="b488f-108">Type: **[**LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**</span></span>

<span data-ttu-id="b488f-109">Указатель на объект шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="b488f-109">A pointer to a vertex shader object.</span></span> <span data-ttu-id="b488f-110">См. [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span><span class="sxs-lookup"><span data-stu-id="b488f-110">See [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b488f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b488f-111">Return value</span></span>

<span data-ttu-id="b488f-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b488f-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b488f-113">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b488f-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="b488f-114">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="b488f-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="b488f-115">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="b488f-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="b488f-116">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетвертексшадер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b488f-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="b488f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b488f-117">Requirements</span></span>



| <span data-ttu-id="b488f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b488f-118">Requirement</span></span> | <span data-ttu-id="b488f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b488f-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b488f-120">Header</span><span class="sxs-lookup"><span data-stu-id="b488f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b488f-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b488f-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b488f-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b488f-122">Library</span></span><br/> | <dl> <span data-ttu-id="b488f-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b488f-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b488f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b488f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b488f-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="b488f-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
