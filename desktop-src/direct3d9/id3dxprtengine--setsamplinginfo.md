---
description: Задает свойства выборки, используемые симулятором предварительно вычисленной радианценой пересылки (PRT).
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: 'Метод ID3DXPRTEngine:: Сетсамплингинфо (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ab229652fe9e333519acce7d8474d3c4f0cf7ef9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821189"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a><span data-ttu-id="70cad-103">Метод ID3DXPRTEngine:: Сетсамплингинфо</span><span class="sxs-lookup"><span data-stu-id="70cad-103">ID3DXPRTEngine::SetSamplingInfo method</span></span>

<span data-ttu-id="70cad-104">Задает свойства выборки, используемые симулятором предварительно вычисленной радианценой пересылки (PRT).</span><span class="sxs-lookup"><span data-stu-id="70cad-104">Sets sampling properties used by the precomputed radiance transfer (PRT) simulator.</span></span>

## <a name="syntax"></a><span data-ttu-id="70cad-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70cad-105">Syntax</span></span>


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a><span data-ttu-id="70cad-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="70cad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70cad-107">*Нумрайс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70cad-107">*NumRays* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70cad-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70cad-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70cad-109">Число лучей, которые нужно направить в каждом примере.</span><span class="sxs-lookup"><span data-stu-id="70cad-109">Number of light rays to direct at each sample.</span></span> <span data-ttu-id="70cad-110">Должен быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="70cad-110">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="70cad-111">*Усесфере* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70cad-111">*UseSphere* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70cad-112">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70cad-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70cad-113">Если **значение — true**, выборки будут вычисляться в полной сфере.</span><span class="sxs-lookup"><span data-stu-id="70cad-113">If **TRUE**, samples will be computed over a full sphere.</span></span> <span data-ttu-id="70cad-114">Если **значение равно false**, выборки будут вычисляться в течение полушария.</span><span class="sxs-lookup"><span data-stu-id="70cad-114">If **FALSE**, samples will be computed over a hemisphere.</span></span>

</dd> <dt>

<span data-ttu-id="70cad-115">*Усекосине* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70cad-115">*UseCosine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70cad-116">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70cad-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70cad-117">Если **значение равно true**, используйте для выборки коэффициент косинуса.</span><span class="sxs-lookup"><span data-stu-id="70cad-117">If **TRUE**, use a cosine weighting of samples.</span></span> <span data-ttu-id="70cad-118">Если оба Усекосине и Усесфере имеют **значение true**, то метод завершится ошибкой и будет возвращена ошибка.</span><span class="sxs-lookup"><span data-stu-id="70cad-118">If both UseCosine and UseSphere are **TRUE**, the method will fail and an error will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="70cad-119">*Адаптивное* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70cad-119">*Adaptive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70cad-120">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70cad-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70cad-121">Значение должно быть **равно false**.</span><span class="sxs-lookup"><span data-stu-id="70cad-121">Must be **FALSE**.</span></span> <span data-ttu-id="70cad-122">Адаптивная выборка в настоящее время не реализована.</span><span class="sxs-lookup"><span data-stu-id="70cad-122">Adaptive sampling is currently not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="70cad-123">*Адаптивесреш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70cad-123">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70cad-124">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70cad-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70cad-125">Не обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="70cad-125">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70cad-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70cad-126">Return value</span></span>

<span data-ttu-id="70cad-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="70cad-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="70cad-128">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="70cad-128">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="70cad-129">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, e \_ Нотимпл, e \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="70cad-129">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_NOTIMPL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="70cad-130">Требования</span><span class="sxs-lookup"><span data-stu-id="70cad-130">Requirements</span></span>



| <span data-ttu-id="70cad-131">Требование</span><span class="sxs-lookup"><span data-stu-id="70cad-131">Requirement</span></span> | <span data-ttu-id="70cad-132">Значение</span><span class="sxs-lookup"><span data-stu-id="70cad-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70cad-133">Header</span><span class="sxs-lookup"><span data-stu-id="70cad-133">Header</span></span><br/>  | <dl> <span data-ttu-id="70cad-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="70cad-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="70cad-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="70cad-135">Library</span></span><br/> | <dl> <span data-ttu-id="70cad-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70cad-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="70cad-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70cad-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70cad-138">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="70cad-138">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
