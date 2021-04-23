---
description: Функция обратного вызова, которая должна быть реализована пользователем для установки массива констант с плавающей точкой шейдера вершин.
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
ms.openlocfilehash: 378af983e0ed7ca1709ae8bb6cfe8615a481b3f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694228"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantf-method"></a><span data-ttu-id="b4b92-103">Метод ID3DXEffectStateManager:: Сетвертексшадерконстантф</span><span class="sxs-lookup"><span data-stu-id="b4b92-103">ID3DXEffectStateManager::SetVertexShaderConstantF method</span></span>

<span data-ttu-id="b4b92-104">Функция обратного вызова, которая должна быть реализована пользователем для установки массива констант с плавающей точкой шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="b4b92-104">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b92-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4b92-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="b4b92-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4b92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4b92-107">*Стартрегистер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4b92-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4b92-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4b92-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4b92-109">Отсчитываемый от нуля индекс первого регистра констант.</span><span class="sxs-lookup"><span data-stu-id="b4b92-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="b4b92-110">*пконстантдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4b92-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4b92-111">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b4b92-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b4b92-112">Массив констант с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="b4b92-112">An array of floating-point constants.</span></span>

</dd> <dt>

<span data-ttu-id="b4b92-113">*Регистеркаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4b92-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4b92-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b4b92-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b4b92-115">Количество регистров в Пконстантдата.</span><span class="sxs-lookup"><span data-stu-id="b4b92-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4b92-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4b92-116">Return value</span></span>

<span data-ttu-id="b4b92-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b4b92-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b4b92-118">Метод, реализуемый пользователем, должен возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b4b92-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="b4b92-119">Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="b4b92-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="b4b92-120">При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="b4b92-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="b4b92-121">Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетвертексшадерконстантф**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b4b92-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4b92-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b4b92-122">Requirements</span></span>



| <span data-ttu-id="b4b92-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b4b92-123">Requirement</span></span> | <span data-ttu-id="b4b92-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b4b92-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b92-125">Header</span><span class="sxs-lookup"><span data-stu-id="b4b92-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b4b92-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4b92-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b4b92-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b4b92-127">Library</span></span><br/> | <dl> <span data-ttu-id="b4b92-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4b92-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b4b92-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4b92-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b92-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="b4b92-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
