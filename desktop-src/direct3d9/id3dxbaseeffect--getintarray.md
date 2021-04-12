---
description: Возвращает массив целых чисел.
ms.assetid: c02b5343-db4f-4e8c-989c-6aba8c19c234
title: 'Метод ID3DXBaseEffect:: Жетинтаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetIntArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f13c6b8717c2108920d7b914da20b99f0451f5d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355900"
---
# <a name="id3dxbaseeffectgetintarray-method"></a><span data-ttu-id="61d2b-103">Метод ID3DXBaseEffect:: Жетинтаррай</span><span class="sxs-lookup"><span data-stu-id="61d2b-103">ID3DXBaseEffect::GetIntArray method</span></span>

<span data-ttu-id="61d2b-104">Возвращает массив целых чисел.</span><span class="sxs-lookup"><span data-stu-id="61d2b-104">Gets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="61d2b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61d2b-105">Syntax</span></span>


```C++
HRESULT GetIntArray(
  [in]  D3DXHANDLE hParameter,
  [out] INT        *pn,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="61d2b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="61d2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61d2b-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="61d2b-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61d2b-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="61d2b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="61d2b-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="61d2b-109">Unique identifier.</span></span> <span data-ttu-id="61d2b-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="61d2b-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="61d2b-111">*PN* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="61d2b-111">*pn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61d2b-112">Тип: **[ **int**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="61d2b-112">Type: **[**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="61d2b-113">Возвращает массив целых чисел.</span><span class="sxs-lookup"><span data-stu-id="61d2b-113">Returns an array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="61d2b-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="61d2b-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61d2b-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="61d2b-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="61d2b-116">Число целочисленных значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="61d2b-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61d2b-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61d2b-117">Return value</span></span>

<span data-ttu-id="61d2b-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="61d2b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="61d2b-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="61d2b-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="61d2b-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="61d2b-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="61d2b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="61d2b-121">Requirements</span></span>



| <span data-ttu-id="61d2b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="61d2b-122">Requirement</span></span> | <span data-ttu-id="61d2b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="61d2b-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61d2b-124">Header</span><span class="sxs-lookup"><span data-stu-id="61d2b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="61d2b-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="61d2b-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="61d2b-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="61d2b-126">Library</span></span><br/> | <dl> <span data-ttu-id="61d2b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61d2b-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="61d2b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61d2b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61d2b-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="61d2b-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="61d2b-130">**сетинтаррай**</span><span class="sxs-lookup"><span data-stu-id="61d2b-130">**SetIntArray**</span></span>](id3dxbaseeffect--setintarray.md)
</dt> </dl>

 

 
