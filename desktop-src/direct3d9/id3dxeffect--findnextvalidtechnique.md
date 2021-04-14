---
description: Выполняет поиск следующего допустимого метода, начиная с метода после указанного метода.
ms.assetid: 0d2f3f80-90fd-495d-acb8-075f50e9a974
title: 'Метод ID3DXEffect:: Финднекствалидтечникуе (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.FindNextValidTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: adcaaa5194abeb17d110118de922811eb84af7fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424413"
---
# <a name="id3dxeffectfindnextvalidtechnique-method"></a><span data-ttu-id="2c790-103">Метод ID3DXEffect:: Финднекствалидтечникуе</span><span class="sxs-lookup"><span data-stu-id="2c790-103">ID3DXEffect::FindNextValidTechnique method</span></span>

<span data-ttu-id="2c790-104">Выполняет поиск следующего допустимого метода, начиная с метода после указанного метода.</span><span class="sxs-lookup"><span data-stu-id="2c790-104">Searches for the next valid technique, starting at the technique after the specified technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c790-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c790-105">Syntax</span></span>


```C++
HRESULT FindNextValidTechnique(
  [in]  D3DXHANDLE hTechnique,
  [out] D3DXHANDLE *pTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="2c790-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c790-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c790-107">*хтечникуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2c790-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c790-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2c790-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2c790-109">Уникальный идентификатор для метода.</span><span class="sxs-lookup"><span data-stu-id="2c790-109">Unique identifier to a technique.</span></span> <span data-ttu-id="2c790-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2c790-110">See [Handles (Direct3D 9)](handles.md).</span></span> <span data-ttu-id="2c790-111">Укажите **значение NULL** для этого параметра, чтобы найти первую допустимую методику.</span><span class="sxs-lookup"><span data-stu-id="2c790-111">Specify **NULL** for this parameter to find the first valid technique.</span></span>

</dd> <dt>

<span data-ttu-id="2c790-112">*птечникуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2c790-112">*pTechnique* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c790-113">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***</span><span class="sxs-lookup"><span data-stu-id="2c790-113">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***</span></span>

<span data-ttu-id="2c790-114">Указатель на идентификатор для следующего метода.</span><span class="sxs-lookup"><span data-stu-id="2c790-114">Pointer to an identifier for the next technique.</span></span> <span data-ttu-id="2c790-115">Если это последний метод, возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="2c790-115">**NULL** is returned if this is the last technique.</span></span> <span data-ttu-id="2c790-116">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2c790-116">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c790-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c790-117">Return value</span></span>

<span data-ttu-id="2c790-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2c790-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2c790-119">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2c790-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2c790-120">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="2c790-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c790-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2c790-121">Requirements</span></span>



| <span data-ttu-id="2c790-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2c790-122">Requirement</span></span> | <span data-ttu-id="2c790-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2c790-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c790-124">Header</span><span class="sxs-lookup"><span data-stu-id="2c790-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2c790-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c790-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2c790-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2c790-126">Library</span></span><br/> | <dl> <span data-ttu-id="2c790-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c790-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2c790-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c790-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c790-129">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="2c790-129">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="2c790-130">**D3DXTECHNIQUE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="2c790-130">**D3DXTECHNIQUE\_DESC**</span></span>](d3dxtechnique-desc.md)
</dt> <dt>

[<span data-ttu-id="2c790-131">**ID3DXEffect:: Валидатетечникуе**</span><span class="sxs-lookup"><span data-stu-id="2c790-131">**ID3DXEffect::ValidateTechnique**</span></span>](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 




