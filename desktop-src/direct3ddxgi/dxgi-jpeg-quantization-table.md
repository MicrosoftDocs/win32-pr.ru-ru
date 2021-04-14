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
# <a name="dxgi_jpeg_quantization_table-structure"></a>\_ \_ Структура таблицы ДИСКРЕТИЗАЦИЯ для DXGI JPEG \_

Описывает таблицу дискретизация JPEG.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct DXGI_JPEG_QUANTIZATION_TABLE {
  BYTE Elements[64];
} DXGI_JPEG_QUANTIZATION_TABLE;
```



## <a name="members"></a>Члены

<dl> <dt>

**Elements (XElement Dynamic Property)** (Elements (Динамическое свойство XElement))
</dt> <dd>

Массив байтов, содержащий элементы таблицы дискретизация.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Дксгитипе. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




