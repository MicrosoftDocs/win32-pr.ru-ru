---
description: 'Метод ID3DXTextureShader:: DESC — Возвращает описание таблицы констант.'
ms.assetid: 91b537bb-5f7a-448b-a21f-c0ddf66d7238
title: 'Метод ID3DXTextureShader:: desc (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ea94f0e22d838f09dae9b423f85aa1d55d2365b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117642"
---
# <a name="id3dxtextureshadergetdesc-method"></a><span data-ttu-id="a7909-103">Метод ID3DXTextureShader:: DESC</span><span class="sxs-lookup"><span data-stu-id="a7909-103">ID3DXTextureShader::GetDesc method</span></span>

<span data-ttu-id="a7909-104">Возвращает описание таблицы констант.</span><span class="sxs-lookup"><span data-stu-id="a7909-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7909-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7909-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="a7909-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7909-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7909-107">*пдеск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7909-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7909-108">Тип: **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="a7909-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="a7909-109">Атрибуты таблицы констант.</span><span class="sxs-lookup"><span data-stu-id="a7909-109">The attributes of the constant table.</span></span> <span data-ttu-id="a7909-110">См. [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="a7909-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7909-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7909-111">Return value</span></span>

<span data-ttu-id="a7909-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a7909-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a7909-113">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a7909-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a7909-114">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="a7909-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7909-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a7909-115">Requirements</span></span>



| <span data-ttu-id="a7909-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a7909-116">Requirement</span></span> | <span data-ttu-id="a7909-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a7909-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7909-118">Header</span><span class="sxs-lookup"><span data-stu-id="a7909-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a7909-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7909-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a7909-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a7909-120">Library</span></span><br/> | <dl> <span data-ttu-id="a7909-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7909-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a7909-122">См. также</span><span class="sxs-lookup"><span data-stu-id="a7909-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7909-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="a7909-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




