---
description: Приложение использует методы этого интерфейса для реализации набора анимации ключевых кадров, хранящегося в сжатом формате данных.
ms.assetid: 858f09b7-c3b6-4e22-8017-ce2d6188ba80
title: Интерфейс ID3DXCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33dd1017859be14924d8d40265696cfb552754ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674703"
---
# <a name="id3dxcompressedanimationset-interface"></a><span data-ttu-id="96c58-103">Интерфейс ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="96c58-103">ID3DXCompressedAnimationSet interface</span></span>

<span data-ttu-id="96c58-104">Приложение использует методы этого интерфейса для реализации набора анимации ключевых кадров, хранящегося в сжатом формате данных.</span><span class="sxs-lookup"><span data-stu-id="96c58-104">An application uses the methods of this interface to implement a key frame animation set stored in a compressed data format.</span></span>

## <a name="members"></a><span data-ttu-id="96c58-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="96c58-105">Members</span></span>

<span data-ttu-id="96c58-106">Интерфейс **ID3DXCompressedAnimationSet** наследует от [**ID3DXAnimationSet**](id3dxanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="96c58-106">The **ID3DXCompressedAnimationSet** interface inherits from [**ID3DXAnimationSet**](id3dxanimationset.md).</span></span> <span data-ttu-id="96c58-107">**ID3DXCompressedAnimationSet** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="96c58-107">**ID3DXCompressedAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="96c58-108">Методы</span><span class="sxs-lookup"><span data-stu-id="96c58-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="96c58-109">Методы</span><span class="sxs-lookup"><span data-stu-id="96c58-109">Methods</span></span>

<span data-ttu-id="96c58-110">Интерфейс **ID3DXCompressedAnimationSet** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="96c58-110">The **ID3DXCompressedAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="96c58-111">Метод</span><span class="sxs-lookup"><span data-stu-id="96c58-111">Method</span></span>                                                                                  | <span data-ttu-id="96c58-112">Описание</span><span class="sxs-lookup"><span data-stu-id="96c58-112">Description</span></span>                                                                      |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="96c58-113">**жеткаллбакккэйс**</span><span class="sxs-lookup"><span data-stu-id="96c58-113">**GetCallbackKeys**</span></span>](id3dxcompressedanimationset--getcallbackkeys.md)                 | <span data-ttu-id="96c58-114">Заполняет массив данными ключа обратного вызова, используемым для анимации ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="96c58-114">Fills an array with callback key data used for key frame animation.</span></span><br/>   |
| [<span data-ttu-id="96c58-115">**жеткомпресседдата**</span><span class="sxs-lookup"><span data-stu-id="96c58-115">**GetCompressedData**</span></span>](id3dxcompressedanimationset--getcompresseddata.md)             | <span data-ttu-id="96c58-116">Возвращает буфер данных, в котором хранятся сжатые данные анимации с помощью ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="96c58-116">Gets the data buffer that stores compressed key frame animation data.</span></span><br/> |
| [<span data-ttu-id="96c58-117">**жетнумкаллбакккэйс**</span><span class="sxs-lookup"><span data-stu-id="96c58-117">**GetNumCallbackKeys**</span></span>](id3dxcompressedanimationset--getnumcallbackkeys.md)           | <span data-ttu-id="96c58-118">Возвращает число ключей обратного вызова в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="96c58-118">Gets the number of callback keys in the animation set.</span></span><br/>                |
| [<span data-ttu-id="96c58-119">**жетплайбакктипе**</span><span class="sxs-lookup"><span data-stu-id="96c58-119">**GetPlaybackType**</span></span>](id3dxcompressedanimationset--getplaybacktype.md)                 | <span data-ttu-id="96c58-120">Возвращает тип цикла воспроизведения набора анимации.</span><span class="sxs-lookup"><span data-stu-id="96c58-120">Gets the type of the animation set playback loop.</span></span><br/>                     |
| [<span data-ttu-id="96c58-121">**жетсаурцетикксперсеконд**</span><span class="sxs-lookup"><span data-stu-id="96c58-121">**GetSourceTicksPerSecond**</span></span>](id3dxcompressedanimationset--getsourcetickspersecond.md) | <span data-ttu-id="96c58-122">Возвращает число тактов кадра анимации, произошедших в секунду.</span><span class="sxs-lookup"><span data-stu-id="96c58-122">Gets the number of animation key frame ticks that occur per second.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="96c58-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96c58-123">Remarks</span></span>

<span data-ttu-id="96c58-124">Создайте набор анимации по ключевым кадрам из сжатого формата с помощью [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="96c58-124">Create a compressed-format key frame animation set with [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).</span></span>

<span data-ttu-id="96c58-125">Тип LPD3DXCOMPRESSEDANIMATIONSET определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="96c58-125">The LPD3DXCOMPRESSEDANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXCompressedAnimationSet ID3DXCompressedAnimationSet;
typedef interface ID3DXCompressedAnimationSet *LPD3DXCOMPRESSEDANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="96c58-126">Требования</span><span class="sxs-lookup"><span data-stu-id="96c58-126">Requirements</span></span>



| <span data-ttu-id="96c58-127">Требование</span><span class="sxs-lookup"><span data-stu-id="96c58-127">Requirement</span></span> | <span data-ttu-id="96c58-128">Значение</span><span class="sxs-lookup"><span data-stu-id="96c58-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96c58-129">Header</span><span class="sxs-lookup"><span data-stu-id="96c58-129">Header</span></span><br/>  | <dl> <span data-ttu-id="96c58-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="96c58-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="96c58-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="96c58-131">Library</span></span><br/> | <dl> <span data-ttu-id="96c58-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96c58-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="96c58-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96c58-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c58-134">**ID3DXAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="96c58-134">**ID3DXAnimationSet**</span></span>](id3dxanimationset.md)
</dt> <dt>

[<span data-ttu-id="96c58-135">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="96c58-135">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




