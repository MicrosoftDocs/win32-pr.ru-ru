---
description: Задает массив значений с плавающей запятой.
ms.assetid: 4b9c27b4-0255-4bbf-9168-491936d64fb9
title: 'Метод ID3DXBaseEffect:: Сетфлоатаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9927f3cd79d7950a94e62881089fb06c67395bac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273695"
---
# <a name="id3dxbaseeffectsetfloatarray-method"></a><span data-ttu-id="9aa5a-103">Метод ID3DXBaseEffect:: Сетфлоатаррай</span><span class="sxs-lookup"><span data-stu-id="9aa5a-103">ID3DXBaseEffect::SetFloatArray method</span></span>

<span data-ttu-id="9aa5a-104">Задает массив значений с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="9aa5a-104">Sets an array of floating point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa5a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9aa5a-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hParameter,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="9aa5a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9aa5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aa5a-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9aa5a-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa5a-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9aa5a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9aa5a-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="9aa5a-109">Unique identifier.</span></span> <span data-ttu-id="9aa5a-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="9aa5a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="9aa5a-111">*Общая папка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9aa5a-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa5a-112">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9aa5a-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9aa5a-113">Массив значений с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="9aa5a-113">Array of floating point values.</span></span>

</dd> <dt>

<span data-ttu-id="9aa5a-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9aa5a-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa5a-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9aa5a-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9aa5a-116">Число значений с плавающей запятой в массиве.</span><span class="sxs-lookup"><span data-stu-id="9aa5a-116">Number of floating point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aa5a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9aa5a-117">Return value</span></span>

<span data-ttu-id="9aa5a-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9aa5a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9aa5a-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9aa5a-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9aa5a-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="9aa5a-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa5a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9aa5a-121">Requirements</span></span>



| <span data-ttu-id="9aa5a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="9aa5a-122">Requirement</span></span> | <span data-ttu-id="9aa5a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9aa5a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa5a-124">Header</span><span class="sxs-lookup"><span data-stu-id="9aa5a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9aa5a-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aa5a-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9aa5a-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9aa5a-126">Library</span></span><br/> | <dl> <span data-ttu-id="9aa5a-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aa5a-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9aa5a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9aa5a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa5a-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="9aa5a-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="9aa5a-130">**жетфлоатаррай**</span><span class="sxs-lookup"><span data-stu-id="9aa5a-130">**GetFloatArray**</span></span>](id3dxbaseeffect--getfloatarray.md)
</dt> </dl>

 

 
