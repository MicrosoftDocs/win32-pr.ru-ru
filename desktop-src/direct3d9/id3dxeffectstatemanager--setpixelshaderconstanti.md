---
description: Функция обратного вызова, которая должна быть реализована пользователем для задания массива целочисленных констант шейдера вершин.
ms.assetid: 55f5747d-b7f8-4d13-ac2c-df2dcb160091
title: 'Метод ID3DXEffectStateManager:: Сетпикселшадерконстанти (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2e84d883370038435dc59bb948ef94fcd82223db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713784"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstanti-method"></a><span data-ttu-id="0b836-103">Метод ID3DXEffectStateManager:: Сетпикселшадерконстанти</span><span class="sxs-lookup"><span data-stu-id="0b836-103">ID3DXEffectStateManager::SetPixelShaderConstantI method</span></span>

<span data-ttu-id="0b836-104">Функция обратного вызова, которая должна быть реализована пользователем для задания массива целочисленных констант шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="0b836-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b836-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b836-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="0b836-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b836-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b836-107">*Стартрегистер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0b836-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b836-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b836-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b836-109">Отсчитываемый от нуля индекс первого регистра констант.</span><span class="sxs-lookup"><span data-stu-id="0b836-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="0b836-110">*пконстантдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0b836-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b836-111">Тип: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0b836-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0b836-112">Массив целочисленных констант.</span><span class="sxs-lookup"><span data-stu-id="0b836-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="0b836-113">*Регистеркаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0b836-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b836-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b836-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b836-115">Количество регистров в Пконстантдата.</span><span class="sxs-lookup"><span data-stu-id="0b836-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b836-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b836-116">Return value</span></span>

<span data-ttu-id="0b836-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b836-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b836-118">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0b836-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="0b836-119">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="0b836-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="0b836-120">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="0b836-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="0b836-121">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетпикселшадерконстанти**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="0b836-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b836-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0b836-122">Requirements</span></span>



| <span data-ttu-id="0b836-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0b836-123">Requirement</span></span> | <span data-ttu-id="0b836-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0b836-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b836-125">Header</span><span class="sxs-lookup"><span data-stu-id="0b836-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0b836-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b836-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="0b836-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0b836-127">Library</span></span><br/> | <dl> <span data-ttu-id="0b836-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b836-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0b836-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b836-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b836-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="0b836-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
