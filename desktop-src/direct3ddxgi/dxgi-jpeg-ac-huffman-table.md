---
description: Описывает таблицу JPEG AC Хаффмана.
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: Структура DXGI_JPEG_AC_HUFFMAN_TABLE (Дксгитипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_AC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 760840822eb6b9411983c72324bc1e86a3208195
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713623"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a><span data-ttu-id="5b60a-103">\_ \_ \_ Структура таблицы Хаффмана для DXGI JPEG AC \_</span><span class="sxs-lookup"><span data-stu-id="5b60a-103">DXGI\_JPEG\_AC\_HUFFMAN\_TABLE structure</span></span>

<span data-ttu-id="5b60a-104">Описывает таблицу JPEG AC Хаффмана.</span><span class="sxs-lookup"><span data-stu-id="5b60a-104">Describes a JPEG AC huffman table.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b60a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b60a-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
```



## <a name="members"></a><span data-ttu-id="5b60a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5b60a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b60a-107">**кодекаунтс**</span><span class="sxs-lookup"><span data-stu-id="5b60a-107">**CodeCounts**</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-108">Количество кодов для каждой длины кода.</span><span class="sxs-lookup"><span data-stu-id="5b60a-108">The number of codes for each code length.</span></span>

</dd> <dt>

<span data-ttu-id="5b60a-109">**кодевалуес**</span><span class="sxs-lookup"><span data-stu-id="5b60a-109">**CodeValues**</span></span>
</dt> <dd>

<span data-ttu-id="5b60a-110">Значения кода Хаффмана в порядке возрастания длины кода.</span><span class="sxs-lookup"><span data-stu-id="5b60a-110">The Huffman code values, in order of increasing code length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b60a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="5b60a-111">Requirements</span></span>



| <span data-ttu-id="5b60a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="5b60a-112">Requirement</span></span> | <span data-ttu-id="5b60a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="5b60a-113">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b60a-114">Header</span><span class="sxs-lookup"><span data-stu-id="5b60a-114">Header</span></span><br/> | <dl> <span data-ttu-id="5b60a-115"><dt>Дксгитипе. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b60a-115"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b60a-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b60a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b60a-117">Структуры DXGI</span><span class="sxs-lookup"><span data-stu-id="5b60a-117">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




