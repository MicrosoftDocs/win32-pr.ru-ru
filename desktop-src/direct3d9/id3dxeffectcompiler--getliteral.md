---
description: Возвращает состояние литерала параметра. Литеральный параметр имеет значение, которое не изменяется в течение времени существования действия.
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: Метод ID3DXEffectCompiler::-Literal (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.GetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c16e3798ab66a34e12812a3560572c45b9206b30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703695"
---
# <a name="id3dxeffectcompilergetliteral-method"></a><span data-ttu-id="aad38-104">Метод ID3DXEffectCompiler::</span><span class="sxs-lookup"><span data-stu-id="aad38-104">ID3DXEffectCompiler::GetLiteral method</span></span>

<span data-ttu-id="aad38-105">Возвращает состояние литерала параметра.</span><span class="sxs-lookup"><span data-stu-id="aad38-105">Gets a literal status of a parameter.</span></span> <span data-ttu-id="aad38-106">Литеральный параметр имеет значение, которое не изменяется в течение времени существования действия.</span><span class="sxs-lookup"><span data-stu-id="aad38-106">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="aad38-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aad38-107">Syntax</span></span>


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="aad38-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aad38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aad38-109">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aad38-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aad38-110">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="aad38-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="aad38-111">Уникальный идентификатор параметра.</span><span class="sxs-lookup"><span data-stu-id="aad38-111">Unique identifier to a parameter.</span></span> <span data-ttu-id="aad38-112">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="aad38-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="aad38-113">*плитерал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aad38-113">*pLiteral* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aad38-114">Тип: **[ **bool** .](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="aad38-114">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="aad38-115">Возвращает значение true, если параметр является литералом, и false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="aad38-115">Returns True if the parameter is a literal, and False otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aad38-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aad38-116">Return value</span></span>

<span data-ttu-id="aad38-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aad38-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aad38-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="aad38-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="aad38-119">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="aad38-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="aad38-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aad38-120">Remarks</span></span>

<span data-ttu-id="aad38-121">Эти методы изменяют только то, является ли параметр литералом.</span><span class="sxs-lookup"><span data-stu-id="aad38-121">This methods only changes whether the parameter is a literal or not.</span></span> <span data-ttu-id="aad38-122">Чтобы изменить значение параметра, используйте такой метод, как [**ID3DXBaseEffect:: сетбул**](id3dxbaseeffect--setbool.md) или [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).</span><span class="sxs-lookup"><span data-stu-id="aad38-122">To change the value of a parameter, use a method like [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) or [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aad38-123">Требования</span><span class="sxs-lookup"><span data-stu-id="aad38-123">Requirements</span></span>



| <span data-ttu-id="aad38-124">Требование</span><span class="sxs-lookup"><span data-stu-id="aad38-124">Requirement</span></span> | <span data-ttu-id="aad38-125">Значение</span><span class="sxs-lookup"><span data-stu-id="aad38-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aad38-126">Header</span><span class="sxs-lookup"><span data-stu-id="aad38-126">Header</span></span><br/>  | <dl> <span data-ttu-id="aad38-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="aad38-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="aad38-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aad38-128">Library</span></span><br/> | <dl> <span data-ttu-id="aad38-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aad38-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="aad38-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aad38-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aad38-131">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="aad38-131">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="aad38-132">Использование и литералы (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="aad38-132">Usages and Literals (Direct3D 9)</span></span>](usages-and-literals.md)
</dt> <dt>

[<span data-ttu-id="aad38-133">**ID3DXEffectCompiler:: Сетлитерал**</span><span class="sxs-lookup"><span data-stu-id="aad38-133">**ID3DXEffectCompiler::SetLiteral**</span></span>](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
