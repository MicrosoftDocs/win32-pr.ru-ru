---
description: Функция обратного вызова, которая должна быть реализована пользователем для задания состояния материала.
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: 'Метод ID3DXEffectStateManager:: Сетматериал (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetMaterial
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b503bd195468fb323e7e655c0bdd201e25dfdce2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694208"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a><span data-ttu-id="43294-103">Метод ID3DXEffectStateManager:: Сетматериал</span><span class="sxs-lookup"><span data-stu-id="43294-103">ID3DXEffectStateManager::SetMaterial method</span></span>

<span data-ttu-id="43294-104">Функция обратного вызова, которая должна быть реализована пользователем для задания состояния материала.</span><span class="sxs-lookup"><span data-stu-id="43294-104">A callback function that must be implemented by a user to set material state.</span></span>

## <a name="syntax"></a><span data-ttu-id="43294-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43294-105">Syntax</span></span>


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a><span data-ttu-id="43294-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43294-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43294-107">*пматериал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43294-107">*pMaterial* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43294-108">Тип: **const [**D3DMATERIAL9**](d3dmaterial9.md) \***</span><span class="sxs-lookup"><span data-stu-id="43294-108">Type: **const [**D3DMATERIAL9**](d3dmaterial9.md)\***</span></span>

<span data-ttu-id="43294-109">Указатель на состояние материала.</span><span class="sxs-lookup"><span data-stu-id="43294-109">A pointer to the material state.</span></span> <span data-ttu-id="43294-110">См. [**D3DMATERIAL9**](d3dmaterial9.md).</span><span class="sxs-lookup"><span data-stu-id="43294-110">See [**D3DMATERIAL9**](d3dmaterial9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43294-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43294-111">Return value</span></span>

<span data-ttu-id="43294-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43294-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43294-113">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="43294-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="43294-114">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="43294-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="43294-115">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="43294-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="43294-116">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетматериал**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="43294-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="43294-117">Требования</span><span class="sxs-lookup"><span data-stu-id="43294-117">Requirements</span></span>



| <span data-ttu-id="43294-118">Требование</span><span class="sxs-lookup"><span data-stu-id="43294-118">Requirement</span></span> | <span data-ttu-id="43294-119">Значение</span><span class="sxs-lookup"><span data-stu-id="43294-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43294-120">Header</span><span class="sxs-lookup"><span data-stu-id="43294-120">Header</span></span><br/>  | <dl> <span data-ttu-id="43294-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="43294-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="43294-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43294-122">Library</span></span><br/> | <dl> <span data-ttu-id="43294-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43294-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="43294-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43294-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43294-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="43294-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
