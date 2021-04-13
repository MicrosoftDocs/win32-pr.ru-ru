---
description: Нарисуйте массив спрайтов.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: 'ID3DX10Sprite: метод:D Равспритесиммедиате (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesImmediate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7fa4012f5f589c7bc0d1f789599da142194f6e08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356120"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a><span data-ttu-id="ceb44-103">ID3DX10Sprite: метод:D Равспритесиммедиате</span><span class="sxs-lookup"><span data-stu-id="ceb44-103">ID3DX10Sprite::DrawSpritesImmediate method</span></span>

<span data-ttu-id="ceb44-104">Нарисуйте массив спрайтов.</span><span class="sxs-lookup"><span data-stu-id="ceb44-104">Draw an array of sprites.</span></span> <span data-ttu-id="ceb44-105">При этом спрайты будут немедленно отправлены на устройство для подготовки к просмотру, что отличается от [**ID3DX10Sprite::D равспритесбуфферед**](id3dx10sprite-drawspritesbuffered.md) , который добавляет массив спрайтов в пакет спрайтов для подготовки к просмотру при вызове [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) .</span><span class="sxs-lookup"><span data-stu-id="ceb44-105">This will immediately send the sprites to the device for rendering, which is different from [**ID3DX10Sprite::DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md) which only adds an array of sprites to a batch of sprites to be rendered when [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) is called.</span></span> <span data-ttu-id="ceb44-106">Этот метод рисования наиболее удобен при рисовании большого количества спрайтов, которые уже были отсортированы в ЦП (или не требуют сортировки), например в системе частиц.</span><span class="sxs-lookup"><span data-stu-id="ceb44-106">This draw method is most useful when drawing a large number of sprites that have already been sorted on the CPU (or do not need to be sorted), such as in a particle system.</span></span> <span data-ttu-id="ceb44-107">Этот метод должен вызываться между вызовами [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) и [**ID3DX10Sprite:: end**](id3dx10sprite-end.md).</span><span class="sxs-lookup"><span data-stu-id="ceb44-107">This must be called in between calls to [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) and [**ID3DX10Sprite::End**](id3dx10sprite-end.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ceb44-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ceb44-108">Syntax</span></span>


```C++
HRESULT DrawSpritesImmediate(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites,
  [in] UINT          cbSprite,
  [in] UINT          flags
);
```



## <a name="parameters"></a><span data-ttu-id="ceb44-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ceb44-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceb44-110">*пспритес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ceb44-110">*pSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceb44-111">Тип: **[ **D3DX10 \_ спрайт**](d3dx10-sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="ceb44-111">Type: **[**D3DX10\_SPRITE**](d3dx10-sprite.md)\***</span></span>

<span data-ttu-id="ceb44-112">Массив спрайтов для рисования.</span><span class="sxs-lookup"><span data-stu-id="ceb44-112">The array of sprites to draw.</span></span> <span data-ttu-id="ceb44-113">См. [**D3DX10 \_ Sprite**](d3dx10-sprite.md).</span><span class="sxs-lookup"><span data-stu-id="ceb44-113">See [**D3DX10\_SPRITE**](d3dx10-sprite.md).</span></span>

</dd> <dt>

<span data-ttu-id="ceb44-114">*кспритес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ceb44-114">*cSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceb44-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ceb44-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ceb44-116">Число спрайтов в Пспритес.</span><span class="sxs-lookup"><span data-stu-id="ceb44-116">The number of sprites in pSprites.</span></span>

</dd> <dt>

<span data-ttu-id="ceb44-117">*кбсприте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ceb44-117">*cbSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceb44-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ceb44-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ceb44-119">Размер структуры спрайта, передаваемых в Пспритес.</span><span class="sxs-lookup"><span data-stu-id="ceb44-119">The size of the sprite structure you are passing into pSprites.</span></span> <span data-ttu-id="ceb44-120">Передача 0 эквивалентна передаче в sizeof (D3DX10 \_ Sprite).</span><span class="sxs-lookup"><span data-stu-id="ceb44-120">Passing in 0 is the equivalent of passing in sizeof(D3DX10\_SPRITE).</span></span>

</dd> <dt>

<span data-ttu-id="ceb44-121">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ceb44-121">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceb44-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ceb44-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ceb44-123">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="ceb44-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceb44-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ceb44-124">Return value</span></span>

<span data-ttu-id="ceb44-125">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ceb44-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ceb44-126">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="ceb44-126">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ceb44-127">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="ceb44-127">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceb44-128">Требования</span><span class="sxs-lookup"><span data-stu-id="ceb44-128">Requirements</span></span>



| <span data-ttu-id="ceb44-129">Требование</span><span class="sxs-lookup"><span data-stu-id="ceb44-129">Requirement</span></span> | <span data-ttu-id="ceb44-130">Значение</span><span class="sxs-lookup"><span data-stu-id="ceb44-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb44-131">Header</span><span class="sxs-lookup"><span data-stu-id="ceb44-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ceb44-132"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ceb44-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ceb44-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ceb44-133">Library</span></span><br/> | <dl> <span data-ttu-id="ceb44-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ceb44-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceb44-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ceb44-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb44-136">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="ceb44-136">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="ceb44-137">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="ceb44-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
