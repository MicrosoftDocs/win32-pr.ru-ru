---
description: Возвращает указатель на поток функции DWORD.
ms.assetid: a051b51a-185c-4a9e-a8b9-4096615e2634
title: Метод ID3DXTextureShader::-Function (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetFunction
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80e504e65e4c8437247b2935794025e1b693433a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703935"
---
# <a name="id3dxtextureshadergetfunction-method"></a><span data-ttu-id="cef1b-103">Метод ID3DXTextureShader:: Function</span><span class="sxs-lookup"><span data-stu-id="cef1b-103">ID3DXTextureShader::GetFunction method</span></span>

<span data-ttu-id="cef1b-104">Возвращает указатель на поток функции DWORD.</span><span class="sxs-lookup"><span data-stu-id="cef1b-104">Gets a pointer to the function DWORD stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="cef1b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cef1b-105">Syntax</span></span>


```C++
HRESULT GetFunction(
  [in] LPD3DXBUFFER *ppFunction
);
```



## <a name="parameters"></a><span data-ttu-id="cef1b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cef1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cef1b-107">*ппфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cef1b-107">*ppFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cef1b-108">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cef1b-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cef1b-109">Указатель на поток функции DWORD.</span><span class="sxs-lookup"><span data-stu-id="cef1b-109">A pointer to the function DWORD stream.</span></span> <span data-ttu-id="cef1b-110">См. [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="cef1b-110">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cef1b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cef1b-111">Return value</span></span>

<span data-ttu-id="cef1b-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cef1b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cef1b-113">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="cef1b-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cef1b-114">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="cef1b-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="cef1b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cef1b-115">Requirements</span></span>



| <span data-ttu-id="cef1b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cef1b-116">Requirement</span></span> | <span data-ttu-id="cef1b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cef1b-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cef1b-118">Header</span><span class="sxs-lookup"><span data-stu-id="cef1b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cef1b-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="cef1b-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="cef1b-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cef1b-120">Library</span></span><br/> | <dl> <span data-ttu-id="cef1b-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cef1b-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cef1b-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cef1b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cef1b-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="cef1b-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




