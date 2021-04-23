---
description: Функция обратного вызова, которая должна быть реализована пользователем для задания массива логических констант шейдера вершин.
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
ms.openlocfilehash: 1eaf68f27d477aee36bd7773488f34bad29db61d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694206"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantb-method"></a><span data-ttu-id="dd359-103">Метод ID3DXEffectStateManager:: Сетвертексшадерконстантб</span><span class="sxs-lookup"><span data-stu-id="dd359-103">ID3DXEffectStateManager::SetVertexShaderConstantB method</span></span>

<span data-ttu-id="dd359-104">Функция обратного вызова, которая должна быть реализована пользователем для задания массива логических констант шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="dd359-104">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd359-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd359-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="dd359-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd359-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd359-107">*Стартрегистер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dd359-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd359-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd359-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dd359-109">Отсчитываемый от нуля индекс первого регистра констант.</span><span class="sxs-lookup"><span data-stu-id="dd359-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="dd359-110">*пконстантдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dd359-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd359-111">Тип: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="dd359-111">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dd359-112">Массив логических констант.</span><span class="sxs-lookup"><span data-stu-id="dd359-112">An array of Boolean constants.</span></span>

</dd> <dt>

<span data-ttu-id="dd359-113">*Регистеркаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dd359-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd359-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd359-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dd359-115">Количество регистров в Пконстантдата.</span><span class="sxs-lookup"><span data-stu-id="dd359-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd359-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd359-116">Return value</span></span>

<span data-ttu-id="dd359-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dd359-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dd359-118">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="dd359-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="dd359-119">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="dd359-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="dd359-120">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="dd359-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="dd359-121">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетвертексшадерконстантб**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="dd359-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd359-122">Требования</span><span class="sxs-lookup"><span data-stu-id="dd359-122">Requirements</span></span>



| <span data-ttu-id="dd359-123">Требование</span><span class="sxs-lookup"><span data-stu-id="dd359-123">Requirement</span></span> | <span data-ttu-id="dd359-124">Значение</span><span class="sxs-lookup"><span data-stu-id="dd359-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd359-125">Header</span><span class="sxs-lookup"><span data-stu-id="dd359-125">Header</span></span><br/>  | <dl> <span data-ttu-id="dd359-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd359-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="dd359-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dd359-127">Library</span></span><br/> | <dl> <span data-ttu-id="dd359-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd359-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dd359-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd359-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd359-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="dd359-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
