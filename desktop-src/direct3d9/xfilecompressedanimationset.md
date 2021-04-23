---
description: Определяет данные анимации сжатых ключевых кадров.
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: Структура КСФИЛЕКОМПРЕССЕДАНИМАТИОНСЕТ (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XFILECOMPRESSEDANIMATIONSET
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 240cac57c9c0d123203ee4599c14092df1327f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105684984"
---
# <a name="xfilecompressedanimationset-structure"></a><span data-ttu-id="33e3a-103">Структура КСФИЛЕКОМПРЕССЕДАНИМАТИОНСЕТ</span><span class="sxs-lookup"><span data-stu-id="33e3a-103">XFILECOMPRESSEDANIMATIONSET structure</span></span>

<span data-ttu-id="33e3a-104">Определяет данные анимации сжатых ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="33e3a-104">Identifies compressed key frame animation data.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e3a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33e3a-105">Syntax</span></span>


```C++
typedef struct XFILECOMPRESSEDANIMATIONSET {
  DWORD CompressedBlockSize;
  FLOAT TicksPerSec;
  DWORD PlaybackType;
  DWORD BufferLength;
} XFILECOMPRESSEDANIMATIONSET, *LPXFILECOMPRESSEDANIMATIONSET;
```



## <a name="members"></a><span data-ttu-id="33e3a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="33e3a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="33e3a-107">**компресседблокксизе**</span><span class="sxs-lookup"><span data-stu-id="33e3a-107">**CompressedBlockSize**</span></span>
</dt> <dd>

<span data-ttu-id="33e3a-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33e3a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33e3a-109">Общий размер (в байтах) сжатых данных в буфере данных анимации сжатого опорного кадра.</span><span class="sxs-lookup"><span data-stu-id="33e3a-109">Total size, in bytes, of the compressed data in the compressed key frame animation data buffer.</span></span>

</dd> <dt>

<span data-ttu-id="33e3a-110">**тикксперсек**</span><span class="sxs-lookup"><span data-stu-id="33e3a-110">**TicksPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="33e3a-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33e3a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33e3a-112">Число тактов кадра анимации, которые находятся в секунду.</span><span class="sxs-lookup"><span data-stu-id="33e3a-112">Number of animation key frame ticks that occur per second.</span></span>

</dd> <dt>

<span data-ttu-id="33e3a-113">**плайбакктипе**</span><span class="sxs-lookup"><span data-stu-id="33e3a-113">**PlaybackType**</span></span>
</dt> <dd>

<span data-ttu-id="33e3a-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33e3a-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33e3a-115">Тип цикла воспроизведения набора анимации.</span><span class="sxs-lookup"><span data-stu-id="33e3a-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="33e3a-116">См. раздел [**\_ тип D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="33e3a-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="33e3a-117">**BufferLength**</span><span class="sxs-lookup"><span data-stu-id="33e3a-117">**BufferLength**</span></span>
</dt> <dd>

<span data-ttu-id="33e3a-118">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33e3a-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33e3a-119">Минимальный размер буфера (в байтах), необходимый для хранения данных анимации с сжатыми ключевыми кадрами.</span><span class="sxs-lookup"><span data-stu-id="33e3a-119">Minimum buffer size, in bytes, required to hold compressed key frame animation data.</span></span> <span data-ttu-id="33e3a-120">Значение равно ((Компресседблокксизе + 3)/4).</span><span class="sxs-lookup"><span data-stu-id="33e3a-120">Value is equal to ( ( CompressedBlockSize + 3 ) / 4 ).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33e3a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="33e3a-121">Requirements</span></span>



| <span data-ttu-id="33e3a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="33e3a-122">Requirement</span></span> | <span data-ttu-id="33e3a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="33e3a-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33e3a-124">Header</span><span class="sxs-lookup"><span data-stu-id="33e3a-124">Header</span></span><br/> | <dl> <span data-ttu-id="33e3a-125"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="33e3a-125"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33e3a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33e3a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e3a-127">Структуры файлов D3DX X</span><span class="sxs-lookup"><span data-stu-id="33e3a-127">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="33e3a-128">**ID3DXCompressedAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="33e3a-128">**ID3DXCompressedAnimationSet**</span></span>](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
