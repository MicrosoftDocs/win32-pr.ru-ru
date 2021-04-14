---
description: Задает массив логических значений.
ms.assetid: 920b3482-cc30-4ab2-bfce-59f03afe11da
title: 'Метод ID3DXBaseEffect:: Сетбуларрай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 813259fc9fcca954c4d7a992c7542387be33bb6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647806"
---
# <a name="id3dxbaseeffectsetboolarray-method"></a><span data-ttu-id="826f2-103">Метод ID3DXBaseEffect:: Сетбуларрай</span><span class="sxs-lookup"><span data-stu-id="826f2-103">ID3DXBaseEffect::SetBoolArray method</span></span>

<span data-ttu-id="826f2-104">Задает массив логических значений.</span><span class="sxs-lookup"><span data-stu-id="826f2-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="826f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="826f2-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hParameter,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="826f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="826f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="826f2-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="826f2-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="826f2-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="826f2-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="826f2-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="826f2-109">Unique identifier.</span></span> <span data-ttu-id="826f2-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="826f2-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="826f2-111">*Pb* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="826f2-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="826f2-112">Тип: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="826f2-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="826f2-113">Массив логических значений.</span><span class="sxs-lookup"><span data-stu-id="826f2-113">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="826f2-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="826f2-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="826f2-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="826f2-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="826f2-116">Число логических значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="826f2-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="826f2-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="826f2-117">Return value</span></span>

<span data-ttu-id="826f2-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="826f2-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="826f2-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="826f2-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="826f2-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="826f2-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="826f2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="826f2-121">Requirements</span></span>



| <span data-ttu-id="826f2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="826f2-122">Requirement</span></span> | <span data-ttu-id="826f2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="826f2-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="826f2-124">Header</span><span class="sxs-lookup"><span data-stu-id="826f2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="826f2-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="826f2-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="826f2-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="826f2-126">Library</span></span><br/> | <dl> <span data-ttu-id="826f2-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="826f2-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="826f2-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="826f2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826f2-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="826f2-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="826f2-130">**жетбуларрай**</span><span class="sxs-lookup"><span data-stu-id="826f2-130">**GetBoolArray**</span></span>](id3dxbaseeffect--getboolarray.md)
</dt> </dl>

 

 
