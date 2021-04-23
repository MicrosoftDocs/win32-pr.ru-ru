---
description: Ресамплинг входного буфера ID3DXPRTBuffer и сохранение его в выходной буфер. Этот метод можно использовать для преобразования буфера вершин в буфер текстуры и наоборот. Он также может использоваться для преобразования одноканальных буферов в 3-канальные буферы и наоборот.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: 'Метод ID3DXPRTEngine:: Ресамплебуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ResampleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8517d04be1d63159a2548935f3e09c12e646775
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821412"
---
# <a name="id3dxprtengineresamplebuffer-method"></a><span data-ttu-id="ab8c4-105">Метод ID3DXPRTEngine:: Ресамплебуффер</span><span class="sxs-lookup"><span data-stu-id="ab8c4-105">ID3DXPRTEngine::ResampleBuffer method</span></span>

<span data-ttu-id="ab8c4-106">Ресамплинг входного буфера [**ID3DXPRTBuffer**](id3dxprtbuffer.md) и сохранение его в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="ab8c4-106">Resamples an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer and saves it to an output buffer.</span></span> <span data-ttu-id="ab8c4-107">Этот метод можно использовать для преобразования буфера вершин в буфер текстуры и наоборот.</span><span class="sxs-lookup"><span data-stu-id="ab8c4-107">This method can be used to convert a vertex buffer to a texture buffer and vice-versa.</span></span> <span data-ttu-id="ab8c4-108">Он также может использоваться для преобразования одноканальных буферов в 3-канальные буферы и наоборот.</span><span class="sxs-lookup"><span data-stu-id="ab8c4-108">It can also be used to convert single-channel buffers to 3-channel buffers and vice-versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab8c4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab8c4-109">Syntax</span></span>


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a><span data-ttu-id="ab8c4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab8c4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab8c4-111">*пбуфферин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ab8c4-111">*pBufferIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab8c4-112">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="ab8c4-112">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="ab8c4-113">Указатель на входной буфер [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ab8c4-113">Pointer to the input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ab8c4-114">*пбуффераут* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ab8c4-114">*pBufferOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab8c4-115">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="ab8c4-115">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="ab8c4-116">Указатель на выходной буфер [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ab8c4-116">Pointer to the output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab8c4-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab8c4-117">Return value</span></span>

<span data-ttu-id="ab8c4-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab8c4-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab8c4-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="ab8c4-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ab8c4-120">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ab8c4-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab8c4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ab8c4-121">Requirements</span></span>



| <span data-ttu-id="ab8c4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ab8c4-122">Requirement</span></span> | <span data-ttu-id="ab8c4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ab8c4-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab8c4-124">Header</span><span class="sxs-lookup"><span data-stu-id="ab8c4-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ab8c4-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab8c4-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ab8c4-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ab8c4-126">Library</span></span><br/> | <dl> <span data-ttu-id="ab8c4-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab8c4-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab8c4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab8c4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab8c4-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="ab8c4-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 




