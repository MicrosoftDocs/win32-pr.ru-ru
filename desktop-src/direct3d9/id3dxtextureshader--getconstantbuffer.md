---
description: Возвращает указатель на таблицу констант.
ms.assetid: 5d836d99-783f-41e1-b7bf-d874d09a4892
title: 'Метод ID3DXTextureShader:: Жетконстантбуффер (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c83a723dde56fc80f643d7209c56fc05ad6cce5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354500"
---
# <a name="id3dxtextureshadergetconstantbuffer-method"></a><span data-ttu-id="1ffee-103">Метод ID3DXTextureShader:: Жетконстантбуффер</span><span class="sxs-lookup"><span data-stu-id="1ffee-103">ID3DXTextureShader::GetConstantBuffer method</span></span>

<span data-ttu-id="1ffee-104">Возвращает указатель на таблицу констант.</span><span class="sxs-lookup"><span data-stu-id="1ffee-104">Get a pointer to the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ffee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ffee-105">Syntax</span></span>


```C++
HRESULT GetConstantBuffer(
  [out] LPD3DXBUFFER *ppConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="1ffee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ffee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ffee-107">*ппконстантбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1ffee-107">*ppConstantBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ffee-108">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ffee-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1ffee-109">Указатель на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) , который содержит константы.</span><span class="sxs-lookup"><span data-stu-id="1ffee-109">Pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains the constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ffee-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ffee-110">Return value</span></span>

<span data-ttu-id="1ffee-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ffee-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ffee-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1ffee-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1ffee-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="1ffee-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ffee-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1ffee-114">Requirements</span></span>



| <span data-ttu-id="1ffee-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1ffee-115">Requirement</span></span> | <span data-ttu-id="1ffee-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1ffee-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ffee-117">Header</span><span class="sxs-lookup"><span data-stu-id="1ffee-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1ffee-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ffee-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1ffee-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1ffee-119">Library</span></span><br/> | <dl> <span data-ttu-id="1ffee-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ffee-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1ffee-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ffee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ffee-122">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="1ffee-122">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




