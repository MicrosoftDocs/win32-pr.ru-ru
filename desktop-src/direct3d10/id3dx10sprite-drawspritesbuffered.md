---
description: Добавьте массив спрайтов в пакет спрайтов для подготовки к просмотру.
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: 'ID3DX10Sprite: метод:D Равспритесбуфферед (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesBuffered
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72893f6a8c3cf82c67f014b4bdbb9a92453de319
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714042"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a><span data-ttu-id="3797e-103">ID3DX10Sprite: метод:D Равспритесбуфферед</span><span class="sxs-lookup"><span data-stu-id="3797e-103">ID3DX10Sprite::DrawSpritesBuffered method</span></span>

<span data-ttu-id="3797e-104">Добавьте массив спрайтов в пакет спрайтов для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="3797e-104">Add an array of sprites to the batch of sprites to be rendered.</span></span> <span data-ttu-id="3797e-105">Этот метод должен вызываться между вызовами [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) и [**ID3DX10Sprite:: end**](id3dx10sprite-end.md), а [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) должен вызываться перед окончанием передачи всех пакетных спрайтов на устройство для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="3797e-105">This must be called in between calls to [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) and [**ID3DX10Sprite::End**](id3dx10sprite-end.md), and [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) must be called before End to send all of the batched sprites to the device for rendering.</span></span> <span data-ttu-id="3797e-106">Этот метод рисования наиболее удобен при рисовании небольшого числа спрайтов, которые нужно поместить в буфер крупного пакета, например шрифтов.</span><span class="sxs-lookup"><span data-stu-id="3797e-106">This draw method is most useful when drawing a small number of sprites that you want buffered into a large batch, such as fonts.</span></span>

## <a name="syntax"></a><span data-ttu-id="3797e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3797e-107">Syntax</span></span>


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
);
```



## <a name="parameters"></a><span data-ttu-id="3797e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3797e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3797e-109">*пспритес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3797e-109">*pSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3797e-110">Тип: **[ **D3DX10 \_ спрайт**](d3dx10-sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="3797e-110">Type: **[**D3DX10\_SPRITE**](d3dx10-sprite.md)\***</span></span>

<span data-ttu-id="3797e-111">Массив спрайтов для рисования.</span><span class="sxs-lookup"><span data-stu-id="3797e-111">The array of sprites to draw.</span></span> <span data-ttu-id="3797e-112">См. [**D3DX10 \_ Sprite**](d3dx10-sprite.md).</span><span class="sxs-lookup"><span data-stu-id="3797e-112">See [**D3DX10\_SPRITE**](d3dx10-sprite.md).</span></span>

</dd> <dt>

<span data-ttu-id="3797e-113">*кспритес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3797e-113">*cSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3797e-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3797e-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3797e-115">Число спрайтов в Пспритес.</span><span class="sxs-lookup"><span data-stu-id="3797e-115">The number of sprites in pSprites.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3797e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3797e-116">Return value</span></span>

<span data-ttu-id="3797e-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3797e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3797e-118">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="3797e-118">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3797e-119">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="3797e-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="3797e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="3797e-120">Requirements</span></span>



| <span data-ttu-id="3797e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="3797e-121">Requirement</span></span> | <span data-ttu-id="3797e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3797e-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3797e-123">Header</span><span class="sxs-lookup"><span data-stu-id="3797e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3797e-124"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="3797e-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3797e-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3797e-125">Library</span></span><br/> | <dl> <span data-ttu-id="3797e-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3797e-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3797e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3797e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3797e-128">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="3797e-128">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="3797e-129">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="3797e-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
