---
description: 'Метод ID3DXEffectStateManager:: Сетвертексшадерконстантб — функция обратного вызова, которая должна быть реализована пользователем для установки массива логических констант шейдера вершин.'
ms.assetid: 25fd0c68-11b5-4401-a2f8-86075ba3fa54
title: 'Метод ID3DXEffectStateManager:: Сетвертексшадерконстантб (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 79d4972c301d7333869d68d36267186a67b37eb1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090412"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantb-method"></a><span data-ttu-id="7edb0-103">Метод ID3DXEffectStateManager:: Сетвертексшадерконстантб</span><span class="sxs-lookup"><span data-stu-id="7edb0-103">ID3DXEffectStateManager::SetVertexShaderConstantB method</span></span>

<span data-ttu-id="7edb0-104">Функция обратного вызова, которая должна быть реализована пользователем для задания массива логических констант шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="7edb0-104">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="7edb0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7edb0-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="7edb0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7edb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7edb0-107">*Стартрегистер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7edb0-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7edb0-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7edb0-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7edb0-109">Отсчитываемый от нуля индекс первого регистра констант.</span><span class="sxs-lookup"><span data-stu-id="7edb0-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="7edb0-110">*пконстантдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7edb0-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7edb0-111">Тип: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="7edb0-111">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7edb0-112">Массив логических констант.</span><span class="sxs-lookup"><span data-stu-id="7edb0-112">An array of Boolean constants.</span></span>

</dd> <dt>

<span data-ttu-id="7edb0-113">*Регистеркаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7edb0-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7edb0-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7edb0-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7edb0-115">Количество регистров в Пконстантдата.</span><span class="sxs-lookup"><span data-stu-id="7edb0-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7edb0-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7edb0-116">Return value</span></span>

<span data-ttu-id="7edb0-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7edb0-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7edb0-118">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7edb0-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="7edb0-119">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="7edb0-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="7edb0-120">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="7edb0-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="7edb0-121">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетвертексшадерконстантб**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="7edb0-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="7edb0-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7edb0-122">Requirements</span></span>



| <span data-ttu-id="7edb0-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7edb0-123">Requirement</span></span> | <span data-ttu-id="7edb0-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7edb0-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7edb0-125">Header</span><span class="sxs-lookup"><span data-stu-id="7edb0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7edb0-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7edb0-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7edb0-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7edb0-127">Library</span></span><br/> | <dl> <span data-ttu-id="7edb0-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7edb0-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7edb0-129">См. также</span><span class="sxs-lookup"><span data-stu-id="7edb0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7edb0-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="7edb0-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
