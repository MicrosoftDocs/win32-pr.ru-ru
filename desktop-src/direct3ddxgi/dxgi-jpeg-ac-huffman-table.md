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
ms.openlocfilehash: 21e279e4974d221a6feba6f135343d122f30f3da1edb18210e0e14f92fdb94a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518377"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a>\_ \_ \_ Структура таблицы Хаффмана для DXGI JPEG AC \_

Описывает таблицу JPEG AC Хаффмана.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
```



## <a name="members"></a>Члены

<dl> <dt>

**кодекаунтс**
</dt> <dd>

Количество кодов для каждой длины кода.

</dd> <dt>

**кодевалуес**
</dt> <dd>

Значения кода Хаффмана в порядке возрастания длины кода.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Дксгитипе. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




