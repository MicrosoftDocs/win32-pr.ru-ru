---
description: Возвращает массив значений типа BOOL.
ms.assetid: 4a5e2f48-fa82-47dc-a388-02a8679585d2
title: 'Метод ID3DXBaseEffect:: Жетбуларрай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f714dfa91baba14524f12b6c3b2cb85211484cf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647893"
---
# <a name="id3dxbaseeffectgetboolarray-method"></a><span data-ttu-id="0a855-103">Метод ID3DXBaseEffect:: Жетбуларрай</span><span class="sxs-lookup"><span data-stu-id="0a855-103">ID3DXBaseEffect::GetBoolArray method</span></span>

<span data-ttu-id="0a855-104">Возвращает массив значений типа BOOL.</span><span class="sxs-lookup"><span data-stu-id="0a855-104">Gets an array of BOOL values.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a855-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a855-105">Syntax</span></span>


```C++
HRESULT GetBoolArray(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pB,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="0a855-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a855-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a855-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0a855-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a855-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0a855-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0a855-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="0a855-109">Unique identifier.</span></span> <span data-ttu-id="0a855-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="0a855-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a855-111">*Pb* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0a855-111">*pB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a855-112">Тип: **[ **bool** .](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a855-112">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0a855-113">Возвращает массив логических значений.</span><span class="sxs-lookup"><span data-stu-id="0a855-113">Returns an array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="0a855-114">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0a855-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a855-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a855-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a855-116">Число логических значений в массиве.</span><span class="sxs-lookup"><span data-stu-id="0a855-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a855-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a855-117">Return value</span></span>

<span data-ttu-id="0a855-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a855-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a855-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0a855-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0a855-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="0a855-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a855-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0a855-121">Requirements</span></span>



| <span data-ttu-id="0a855-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0a855-122">Requirement</span></span> | <span data-ttu-id="0a855-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0a855-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a855-124">Header</span><span class="sxs-lookup"><span data-stu-id="0a855-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0a855-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a855-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0a855-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0a855-126">Library</span></span><br/> | <dl> <span data-ttu-id="0a855-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a855-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0a855-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a855-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a855-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="0a855-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="0a855-130">**сетбуларрай**</span><span class="sxs-lookup"><span data-stu-id="0a855-130">**SetBoolArray**</span></span>](id3dxbaseeffect--setboolarray.md)
</dt> </dl>

 

 
