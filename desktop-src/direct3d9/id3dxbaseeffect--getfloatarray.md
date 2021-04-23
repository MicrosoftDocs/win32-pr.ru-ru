---
description: Возвращает массив значений с плавающей запятой.
ms.assetid: ba839129-c332-4ce8-b7c1-ea0ef4697ade
title: 'Метод ID3DXBaseEffect:: Жетфлоатаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloatArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2ea71daa3b207a8f7716bf0a0db3608554c0b9f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355920"
---
# <a name="id3dxbaseeffectgetfloatarray-method"></a><span data-ttu-id="a3bf7-103">Метод ID3DXBaseEffect:: Жетфлоатаррай</span><span class="sxs-lookup"><span data-stu-id="a3bf7-103">ID3DXBaseEffect::GetFloatArray method</span></span>

<span data-ttu-id="a3bf7-104">Возвращает массив значений с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="a3bf7-104">Gets an array of floating point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3bf7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3bf7-105">Syntax</span></span>


```C++
HRESULT GetFloatArray(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="a3bf7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3bf7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3bf7-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3bf7-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3bf7-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a3bf7-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a3bf7-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="a3bf7-109">Unique identifier.</span></span> <span data-ttu-id="a3bf7-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="a3bf7-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3bf7-111">*Общая папка* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a3bf7-111">*pf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3bf7-112">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3bf7-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a3bf7-113">Возвращает массив значений с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="a3bf7-113">Returns an array of floating point values.</span></span>

</dd> <dt>

<span data-ttu-id="a3bf7-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3bf7-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3bf7-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3bf7-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3bf7-116">Число значений с плавающей запятой в массиве.</span><span class="sxs-lookup"><span data-stu-id="a3bf7-116">Number of floating point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3bf7-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3bf7-117">Return value</span></span>

<span data-ttu-id="a3bf7-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3bf7-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3bf7-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a3bf7-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a3bf7-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="a3bf7-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3bf7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a3bf7-121">Requirements</span></span>



| <span data-ttu-id="a3bf7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a3bf7-122">Requirement</span></span> | <span data-ttu-id="a3bf7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a3bf7-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3bf7-124">Header</span><span class="sxs-lookup"><span data-stu-id="a3bf7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a3bf7-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3bf7-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a3bf7-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a3bf7-126">Library</span></span><br/> | <dl> <span data-ttu-id="a3bf7-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3bf7-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a3bf7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3bf7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3bf7-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a3bf7-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="a3bf7-130">**сетфлоатаррай**</span><span class="sxs-lookup"><span data-stu-id="a3bf7-130">**SetFloatArray**</span></span>](id3dxbaseeffect--setfloatarray.md)
</dt> </dl>

 

 
