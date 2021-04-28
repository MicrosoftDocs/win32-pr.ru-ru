---
description: 'Метод ID3DXEffectStateManager:: Сетвертексшадерконстантф — функция обратного вызова, которая должна быть реализована пользователем для установки массива констант с плавающей запятой вершин.'
ms.assetid: 3a13040d-5d5a-4454-bf11-cda9653585c0
title: 'Метод ID3DXEffectStateManager:: Сетвертексшадерконстантф (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ffbad3c695758a0388baf8161c322c1ff423699b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090392"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantf-method"></a><span data-ttu-id="e282b-103">Метод ID3DXEffectStateManager:: Сетвертексшадерконстантф</span><span class="sxs-lookup"><span data-stu-id="e282b-103">ID3DXEffectStateManager::SetVertexShaderConstantF method</span></span>

<span data-ttu-id="e282b-104">Функция обратного вызова, которая должна быть реализована пользователем для установки массива констант с плавающей точкой шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="e282b-104">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="e282b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e282b-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="e282b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e282b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e282b-107">*Стартрегистер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e282b-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e282b-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e282b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e282b-109">Отсчитываемый от нуля индекс первого регистра констант.</span><span class="sxs-lookup"><span data-stu-id="e282b-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="e282b-110">*пконстантдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e282b-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e282b-111">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e282b-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e282b-112">Массив констант с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="e282b-112">An array of floating-point constants.</span></span>

</dd> <dt>

<span data-ttu-id="e282b-113">*Регистеркаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e282b-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e282b-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e282b-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e282b-115">Количество регистров в Пконстантдата.</span><span class="sxs-lookup"><span data-stu-id="e282b-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e282b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e282b-116">Return value</span></span>

<span data-ttu-id="e282b-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e282b-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e282b-118">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e282b-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="e282b-119">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="e282b-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="e282b-120">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="e282b-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="e282b-121">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетвертексшадерконстантф**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e282b-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="e282b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e282b-122">Requirements</span></span>



| <span data-ttu-id="e282b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e282b-123">Requirement</span></span> | <span data-ttu-id="e282b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e282b-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e282b-125">Header</span><span class="sxs-lookup"><span data-stu-id="e282b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e282b-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e282b-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e282b-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e282b-127">Library</span></span><br/> | <dl> <span data-ttu-id="e282b-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e282b-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e282b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="e282b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e282b-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="e282b-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
