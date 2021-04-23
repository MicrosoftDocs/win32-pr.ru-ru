---
description: Описывает таблицу Хаффмана контроллера домена JPEG.
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: Структура DXGI_JPEG_DC_HUFFMAN_TABLE (Дксгитипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_DC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: b2f5f73f7c6def745b987818b9ec30fb3e2752e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273751"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a><span data-ttu-id="704f6-103">\_ \_ \_ Структура таблицы ХАФФМАНА DC для DXGI JPEG \_</span><span class="sxs-lookup"><span data-stu-id="704f6-103">DXGI\_JPEG\_DC\_HUFFMAN\_TABLE structure</span></span>

<span data-ttu-id="704f6-104">Описывает таблицу Хаффмана контроллера домена JPEG.</span><span class="sxs-lookup"><span data-stu-id="704f6-104">Describes a JPEG DC huffman table.</span></span>

## <a name="syntax"></a><span data-ttu-id="704f6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="704f6-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_DC_HUFFMAN_TABLE {
  BYTE CodeCounts[12];
  BYTE CodeValues[12];
} DXGI_JPEG_DC_HUFFMAN_TABLE;
```



## <a name="members"></a><span data-ttu-id="704f6-106">Члены</span><span class="sxs-lookup"><span data-stu-id="704f6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="704f6-107">**кодекаунтс**</span><span class="sxs-lookup"><span data-stu-id="704f6-107">**CodeCounts**</span></span>
</dt> <dd>

<span data-ttu-id="704f6-108">Количество кодов для каждой длины кода.</span><span class="sxs-lookup"><span data-stu-id="704f6-108">The number of codes for each code length.</span></span>

</dd> <dt>

<span data-ttu-id="704f6-109">**кодевалуес**</span><span class="sxs-lookup"><span data-stu-id="704f6-109">**CodeValues**</span></span>
</dt> <dd>

<span data-ttu-id="704f6-110">Значения кода Хаффмана в порядке возрастания длины кода.</span><span class="sxs-lookup"><span data-stu-id="704f6-110">The Huffman code values, in order of increasing code length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="704f6-111">Требования</span><span class="sxs-lookup"><span data-stu-id="704f6-111">Requirements</span></span>



| <span data-ttu-id="704f6-112">Требование</span><span class="sxs-lookup"><span data-stu-id="704f6-112">Requirement</span></span> | <span data-ttu-id="704f6-113">Значение</span><span class="sxs-lookup"><span data-stu-id="704f6-113">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="704f6-114">Header</span><span class="sxs-lookup"><span data-stu-id="704f6-114">Header</span></span><br/> | <dl> <span data-ttu-id="704f6-115"><dt>Дксгитипе. h</dt></span><span class="sxs-lookup"><span data-stu-id="704f6-115"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="704f6-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="704f6-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="704f6-117">Структуры DXGI</span><span class="sxs-lookup"><span data-stu-id="704f6-117">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




