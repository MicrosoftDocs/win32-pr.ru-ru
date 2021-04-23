---
description: Возвращает описание метода.
ms.assetid: 12122858-1e54-446c-8f12-20cc62499d74
title: 'Метод ID3DXBaseEffect:: Жеттечникуедеск (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6027cf24576a29a1f447e5c20f99634c42adf00d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273957"
---
# <a name="id3dxbaseeffectgettechniquedesc-method"></a><span data-ttu-id="32444-103">Метод ID3DXBaseEffect:: Жеттечникуедеск</span><span class="sxs-lookup"><span data-stu-id="32444-103">ID3DXBaseEffect::GetTechniqueDesc method</span></span>

<span data-ttu-id="32444-104">Возвращает описание метода.</span><span class="sxs-lookup"><span data-stu-id="32444-104">Gets a technique description.</span></span>

## <a name="syntax"></a><span data-ttu-id="32444-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32444-105">Syntax</span></span>


```C++
HRESULT GetTechniqueDesc(
  [in]  D3DXHANDLE         hTechnique,
  [out] D3DXTECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="32444-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="32444-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32444-107">*хтечникуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="32444-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32444-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="32444-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="32444-109">Обрабатывающий метод.</span><span class="sxs-lookup"><span data-stu-id="32444-109">Technique handle.</span></span> <span data-ttu-id="32444-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="32444-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="32444-111">*пдеск* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="32444-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32444-112">Тип: **[ **D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="32444-112">Type: **[**D3DXTECHNIQUE\_DESC**](d3dxtechnique-desc.md)\***</span></span>

<span data-ttu-id="32444-113">Возвращает описание метода.</span><span class="sxs-lookup"><span data-stu-id="32444-113">Returns a description of the technique.</span></span> <span data-ttu-id="32444-114">См. [**D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md).</span><span class="sxs-lookup"><span data-stu-id="32444-114">See [**D3DXTECHNIQUE\_DESC**](d3dxtechnique-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32444-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32444-115">Return value</span></span>

<span data-ttu-id="32444-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="32444-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="32444-117">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="32444-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="32444-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="32444-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="32444-119">Требования</span><span class="sxs-lookup"><span data-stu-id="32444-119">Requirements</span></span>



| <span data-ttu-id="32444-120">Требование</span><span class="sxs-lookup"><span data-stu-id="32444-120">Requirement</span></span> | <span data-ttu-id="32444-121">Значение</span><span class="sxs-lookup"><span data-stu-id="32444-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="32444-122">Header</span><span class="sxs-lookup"><span data-stu-id="32444-122">Header</span></span><br/>  | <dl> <span data-ttu-id="32444-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="32444-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="32444-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="32444-124">Library</span></span><br/> | <dl> <span data-ttu-id="32444-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32444-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="32444-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32444-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32444-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="32444-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




