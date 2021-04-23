---
description: Функция обратного вызова, которая должна быть реализована пользователем для задания числа сегментов подразделений для N-патчей.
ms.assetid: f94910ee-3385-44d3-b4f1-a0e88c7afa39
title: 'Метод ID3DXEffectStateManager:: Сетнпатчмоде (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetNPatchMode
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9b8725a0482b6945b04013df43d34a502f25b7b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000512"
---
# <a name="id3dxeffectstatemanagersetnpatchmode-method"></a><span data-ttu-id="bfccd-103">Метод ID3DXEffectStateManager:: Сетнпатчмоде</span><span class="sxs-lookup"><span data-stu-id="bfccd-103">ID3DXEffectStateManager::SetNPatchMode method</span></span>

<span data-ttu-id="bfccd-104">Функция обратного вызова, которая должна быть реализована пользователем для задания числа сегментов подразделений для N-патчей.</span><span class="sxs-lookup"><span data-stu-id="bfccd-104">A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfccd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfccd-105">Syntax</span></span>


```C++
HRESULT SetNPatchMode(
  [in] FLOAT nSegments
);
```



## <a name="parameters"></a><span data-ttu-id="bfccd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfccd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfccd-107">*нсегментс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bfccd-107">*nSegments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfccd-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bfccd-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bfccd-109">Разделить поверхность на это число подразделений.</span><span class="sxs-lookup"><span data-stu-id="bfccd-109">Break the surface into this number of subdivisions.</span></span> <span data-ttu-id="bfccd-110">Это то же самое, что и число, используемое [**IDirect3DDevice9:: сетнпатчмоде**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="bfccd-110">This is the same as the number used by [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfccd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bfccd-111">Return value</span></span>

<span data-ttu-id="bfccd-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bfccd-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bfccd-113">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="bfccd-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="bfccd-114">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="bfccd-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="bfccd-115">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="bfccd-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="bfccd-116">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетнпатчмоде**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="bfccd-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfccd-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bfccd-117">Requirements</span></span>



| <span data-ttu-id="bfccd-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bfccd-118">Requirement</span></span> | <span data-ttu-id="bfccd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bfccd-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfccd-120">Header</span><span class="sxs-lookup"><span data-stu-id="bfccd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bfccd-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfccd-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="bfccd-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bfccd-122">Library</span></span><br/> | <dl> <span data-ttu-id="bfccd-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfccd-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bfccd-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bfccd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfccd-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="bfccd-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
