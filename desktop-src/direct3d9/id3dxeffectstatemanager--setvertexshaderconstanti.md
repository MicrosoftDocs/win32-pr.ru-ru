---
description: Функция обратного вызова, которая должна быть реализована пользователем для задания массива целочисленных констант шейдера вершин.
ms.assetid: 0035c97a-1b17-4665-9032-7b3b9a9d2cff
title: 'Метод ID3DXEffectStateManager:: Сетвертексшадерконстанти (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: be95d678ee6b0c44dc49e180df4d3332a84d5fe7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713779"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstanti-method"></a><span data-ttu-id="cc298-103">Метод ID3DXEffectStateManager:: Сетвертексшадерконстанти</span><span class="sxs-lookup"><span data-stu-id="cc298-103">ID3DXEffectStateManager::SetVertexShaderConstantI method</span></span>

<span data-ttu-id="cc298-104">Функция обратного вызова, которая должна быть реализована пользователем для задания массива целочисленных констант шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="cc298-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc298-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc298-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="cc298-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc298-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc298-107">*Стартрегистер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cc298-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc298-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc298-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc298-109">Отсчитываемый от нуля индекс первого регистра констант.</span><span class="sxs-lookup"><span data-stu-id="cc298-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="cc298-110">*пконстантдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cc298-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc298-111">Тип: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cc298-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cc298-112">Массив целочисленных констант.</span><span class="sxs-lookup"><span data-stu-id="cc298-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="cc298-113">*Регистеркаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cc298-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc298-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc298-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc298-115">Количество регистров в Пконстантдата.</span><span class="sxs-lookup"><span data-stu-id="cc298-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc298-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc298-116">Return value</span></span>

<span data-ttu-id="cc298-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc298-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc298-118">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="cc298-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="cc298-119">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="cc298-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="cc298-120">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="cc298-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="cc298-121">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетвертексшадерконстанти**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="cc298-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc298-122">Требования</span><span class="sxs-lookup"><span data-stu-id="cc298-122">Requirements</span></span>



| <span data-ttu-id="cc298-123">Требование</span><span class="sxs-lookup"><span data-stu-id="cc298-123">Requirement</span></span> | <span data-ttu-id="cc298-124">Значение</span><span class="sxs-lookup"><span data-stu-id="cc298-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc298-125">Header</span><span class="sxs-lookup"><span data-stu-id="cc298-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cc298-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc298-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="cc298-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc298-127">Library</span></span><br/> | <dl> <span data-ttu-id="cc298-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc298-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cc298-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc298-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc298-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="cc298-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
