---
description: Возвращает описание параметра или заметки.
ms.assetid: fd54eb08-a7e4-4106-b0ed-49a4da7fcadc
title: 'Метод ID3DXBaseEffect:: Жетпараметердеск (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8c3a52c06ebed764b3ab1718488c2dbc55ceda41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694318"
---
# <a name="id3dxbaseeffectgetparameterdesc-method"></a><span data-ttu-id="f6297-103">Метод ID3DXBaseEffect:: Жетпараметердеск</span><span class="sxs-lookup"><span data-stu-id="f6297-103">ID3DXBaseEffect::GetParameterDesc method</span></span>

<span data-ttu-id="f6297-104">Возвращает описание параметра или заметки.</span><span class="sxs-lookup"><span data-stu-id="f6297-104">Gets a parameter or annotation description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6297-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6297-105">Syntax</span></span>


```C++
HRESULT GetParameterDesc(
  [in]  D3DXHANDLE         hParameter,
  [out] D3DXPARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="f6297-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6297-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6297-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f6297-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6297-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f6297-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f6297-109">Маркер параметра или заметки.</span><span class="sxs-lookup"><span data-stu-id="f6297-109">Parameter or annotation handle.</span></span> <span data-ttu-id="f6297-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f6297-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6297-111">*пдеск* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f6297-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6297-112">Тип: **[ **D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="f6297-112">Type: **[**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md)\***</span></span>

<span data-ttu-id="f6297-113">Возвращает описание указанного параметра или заметки.</span><span class="sxs-lookup"><span data-stu-id="f6297-113">Returns a description of the specified parameter or annotation.</span></span> <span data-ttu-id="f6297-114">См. [**D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md).</span><span class="sxs-lookup"><span data-stu-id="f6297-114">See [**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6297-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6297-115">Return value</span></span>

<span data-ttu-id="f6297-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f6297-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f6297-117">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="f6297-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f6297-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="f6297-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6297-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f6297-119">Requirements</span></span>



| <span data-ttu-id="f6297-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f6297-120">Requirement</span></span> | <span data-ttu-id="f6297-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f6297-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6297-122">Header</span><span class="sxs-lookup"><span data-stu-id="f6297-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f6297-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6297-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f6297-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6297-124">Library</span></span><br/> | <dl> <span data-ttu-id="f6297-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6297-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f6297-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6297-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6297-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="f6297-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




