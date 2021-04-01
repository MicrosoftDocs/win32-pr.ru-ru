---
description: Возвращает шейдер вершин.
ms.assetid: ab58b465-7b10-46eb-88c0-c5229cb09481
title: 'Метод ID3DXBaseEffect:: Жетвертексшадер (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVertexShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ad6bb7cbf7c483ccaffa83b0e828c867026957fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157134"
---
# <a name="id3dxbaseeffectgetvertexshader-method"></a><span data-ttu-id="1c751-103">Метод ID3DXBaseEffect:: Жетвертексшадер</span><span class="sxs-lookup"><span data-stu-id="1c751-103">ID3DXBaseEffect::GetVertexShader method</span></span>

<span data-ttu-id="1c751-104">Возвращает шейдер вершин.</span><span class="sxs-lookup"><span data-stu-id="1c751-104">Gets a vertex shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c751-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c751-105">Syntax</span></span>


```C++
HRESULT GetVertexShader(
  [in]  D3DXHANDLE              hParameter,
  [out] LPDIRECT3DVERTEXSHADER9 *ppVShader
);
```



## <a name="parameters"></a><span data-ttu-id="1c751-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c751-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c751-107">*хпараметер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c751-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c751-108">Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1c751-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1c751-109">Уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="1c751-109">Unique identifier.</span></span> <span data-ttu-id="1c751-110">См. раздел [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="1c751-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c751-111">*ппвшадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1c751-111">*ppVShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c751-112">Тип: **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)\***</span><span class="sxs-lookup"><span data-stu-id="1c751-112">Type: **[**LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)\***</span></span>

<span data-ttu-id="1c751-113">Возвращает объект шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="1c751-113">Returns a vertex shader object.</span></span> <span data-ttu-id="1c751-114">См. [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span><span class="sxs-lookup"><span data-stu-id="1c751-114">See [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c751-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c751-115">Return value</span></span>

<span data-ttu-id="1c751-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1c751-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1c751-117">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1c751-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1c751-118">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="1c751-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c751-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1c751-119">Requirements</span></span>



| <span data-ttu-id="1c751-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1c751-120">Requirement</span></span> | <span data-ttu-id="1c751-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1c751-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c751-122">Header</span><span class="sxs-lookup"><span data-stu-id="1c751-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1c751-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c751-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1c751-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1c751-124">Library</span></span><br/> | <dl> <span data-ttu-id="1c751-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c751-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1c751-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c751-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c751-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="1c751-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
