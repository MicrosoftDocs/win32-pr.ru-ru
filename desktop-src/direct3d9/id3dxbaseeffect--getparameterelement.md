---
description: Получение маркера параметра элемента массива.
ms.assetid: fe8edbc5-dc1d-4386-8149-489541d55bde
title: 'Метод ID3DXBaseEffect:: Жетпараметерелемент (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterElement
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5130ccf57634f9b1a569a1dd70833fe2014e1a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355873"
---
# <a name="id3dxbaseeffectgetparameterelement-method"></a><span data-ttu-id="002e5-103">Метод ID3DXBaseEffect:: Жетпараметерелемент</span><span class="sxs-lookup"><span data-stu-id="002e5-103">ID3DXBaseEffect::GetParameterElement method</span></span>

<span data-ttu-id="002e5-104">Получение маркера параметра элемента массива.</span><span class="sxs-lookup"><span data-stu-id="002e5-104">Get the handle of an array element parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="002e5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="002e5-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterElement(
  [in] D3DXHANDLE hParameter,
  [in] UINT       ElementIndex
);
```



## <a name="parameters"></a><span data-ttu-id="002e5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="002e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="002e5-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="002e5-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002e5-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="002e5-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="002e5-109">Маркер массива.</span><span class="sxs-lookup"><span data-stu-id="002e5-109">Handle of the array.</span></span> <span data-ttu-id="002e5-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="002e5-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="002e5-111">*Елементиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="002e5-111">*ElementIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002e5-112">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="002e5-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="002e5-113">Индекс элемента массива.</span><span class="sxs-lookup"><span data-stu-id="002e5-113">Array element index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="002e5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="002e5-114">Return value</span></span>

<span data-ttu-id="002e5-115">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="002e5-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="002e5-116">Возвращает маркер указанного параметра или **значение NULL** , если значение Хпараметер или елементиндекс недопустимо.</span><span class="sxs-lookup"><span data-stu-id="002e5-116">Returns the handle of the specified parameter, or **NULL** if either hParameter or ElementIndex is invalid.</span></span> <span data-ttu-id="002e5-117">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="002e5-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="002e5-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="002e5-118">Remarks</span></span>

<span data-ttu-id="002e5-119">Этот метод используется для получения элемента параметра, который является массивом.</span><span class="sxs-lookup"><span data-stu-id="002e5-119">This method is used to get an element of a parameter that is an array.</span></span>

## <a name="requirements"></a><span data-ttu-id="002e5-120">Требования</span><span class="sxs-lookup"><span data-stu-id="002e5-120">Requirements</span></span>



| <span data-ttu-id="002e5-121">Требование</span><span class="sxs-lookup"><span data-stu-id="002e5-121">Requirement</span></span> | <span data-ttu-id="002e5-122">Значение</span><span class="sxs-lookup"><span data-stu-id="002e5-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="002e5-123">Header</span><span class="sxs-lookup"><span data-stu-id="002e5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="002e5-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="002e5-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="002e5-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="002e5-125">Library</span></span><br/> | <dl> <span data-ttu-id="002e5-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="002e5-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="002e5-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="002e5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="002e5-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="002e5-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
