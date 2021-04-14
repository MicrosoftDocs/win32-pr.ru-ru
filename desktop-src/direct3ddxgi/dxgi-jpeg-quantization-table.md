---
description: Описывает таблицу дискретизация JPEG.
ms.assetid: DE1AAB15-B0B8-4594-BBCE-5F8EE5CE0AF7
title: Структура DXGI_JPEG_QUANTIZATION_TABLE (Дксгитипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_QUANTIZATION_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b0a097cb4c364ecc14e471f7c15f642aa65e912
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647841"
---
# <a name="dxgi_jpeg_quantization_table-structure"></a><span data-ttu-id="1e290-103">\_ \_ Структура таблицы ДИСКРЕТИЗАЦИЯ для DXGI JPEG \_</span><span class="sxs-lookup"><span data-stu-id="1e290-103">DXGI\_JPEG\_QUANTIZATION\_TABLE structure</span></span>

<span data-ttu-id="1e290-104">Описывает таблицу дискретизация JPEG.</span><span class="sxs-lookup"><span data-stu-id="1e290-104">Describes a JPEG quantization table.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e290-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e290-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_QUANTIZATION_TABLE {
  BYTE Elements[64];
} DXGI_JPEG_QUANTIZATION_TABLE;
```



## <a name="members"></a><span data-ttu-id="1e290-106">Члены</span><span class="sxs-lookup"><span data-stu-id="1e290-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1e290-107">**Elements (XElement Dynamic Property)** (Elements (Динамическое свойство XElement))</span><span class="sxs-lookup"><span data-stu-id="1e290-107">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="1e290-108">Массив байтов, содержащий элементы таблицы дискретизация.</span><span class="sxs-lookup"><span data-stu-id="1e290-108">An array of bytes containing the elements of the quantization table.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e290-109">Требования</span><span class="sxs-lookup"><span data-stu-id="1e290-109">Requirements</span></span>



| <span data-ttu-id="1e290-110">Требование</span><span class="sxs-lookup"><span data-stu-id="1e290-110">Requirement</span></span> | <span data-ttu-id="1e290-111">Значение</span><span class="sxs-lookup"><span data-stu-id="1e290-111">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e290-112">Header</span><span class="sxs-lookup"><span data-stu-id="1e290-112">Header</span></span><br/> | <dl> <span data-ttu-id="1e290-113"><dt>Дксгитипе. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e290-113"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e290-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e290-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e290-115">Структуры DXGI</span><span class="sxs-lookup"><span data-stu-id="1e290-115">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




