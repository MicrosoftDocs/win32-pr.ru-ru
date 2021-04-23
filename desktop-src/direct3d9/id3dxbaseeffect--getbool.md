---
description: Возвращает логическое значение.
ms.assetid: 9d61efcd-f267-4c45-b685-d363588796f7
title: Метод ID3DXBaseEffect::-bool (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0476c62733379a7e92aca55c3cdc2c31a3526de2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713999"
---
# <a name="id3dxbaseeffectgetbool-method"></a><span data-ttu-id="c41be-103">Метод ID3DXBaseEffect::</span><span class="sxs-lookup"><span data-stu-id="c41be-103">ID3DXBaseEffect::GetBool method</span></span>

<span data-ttu-id="c41be-104">Возвращает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="c41be-104">Gets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c41be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c41be-105">Syntax</span></span>


```C++
HRESULT GetBool(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pb
);
```



## <a name="parameters"></a><span data-ttu-id="c41be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c41be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c41be-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c41be-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c41be-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c41be-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c41be-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="c41be-109">Unique identifier.</span></span> <span data-ttu-id="c41be-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c41be-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c41be-111">*Pb* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c41be-111">*pb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c41be-112">Тип: **[ **bool** .](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c41be-112">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c41be-113">Возвращает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="c41be-113">Returns a Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c41be-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c41be-114">Return value</span></span>

<span data-ttu-id="c41be-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c41be-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c41be-116">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c41be-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c41be-117">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="c41be-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c41be-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c41be-118">Requirements</span></span>



| <span data-ttu-id="c41be-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c41be-119">Requirement</span></span> | <span data-ttu-id="c41be-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c41be-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c41be-121">Header</span><span class="sxs-lookup"><span data-stu-id="c41be-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c41be-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c41be-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c41be-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c41be-123">Library</span></span><br/> | <dl> <span data-ttu-id="c41be-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c41be-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c41be-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c41be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c41be-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c41be-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="c41be-127">**сетбул**</span><span class="sxs-lookup"><span data-stu-id="c41be-127">**SetBool**</span></span>](id3dxbaseeffect--setbool.md)
</dt> </dl>

 

 
