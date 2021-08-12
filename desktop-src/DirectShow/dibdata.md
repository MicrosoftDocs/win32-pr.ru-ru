---
description: Структура ДИБДАТА содержит сведения о аппаратно-независимом точечном рисунке (DIB) GDI.
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: Структура ДИБДАТА (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIBDATA
api_type:
- HeaderDef
api_location:
- Winutil.h
ms.openlocfilehash: b4449f45afac56b202e9b23516dc849c6364e8781be7cfbe7cfb2b630bd16921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653822"
---
# <a name="dibdata-structure"></a>Структура ДИБДАТА

`DIBDATA`Структура содержит сведения об аппаратно-независимом точечном рисунке GDI (DIB).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagDIBDATA {
  LONG       PaletteVersion;
  DIBSECTION DibSection;
  HBITMAP    hBitmap;
  HANDLE     hMapping;
  BYTE       *pBase;
} DIBDATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**палеттеверсион**
</dt> <dd>

Этот элемент должен увеличиваться при каждом изменении палитры.

</dd> <dt>

**дибсектион**
</dt> <dd>

Структура **дибсектион** , содержащая сведения об элементе DIB. Дополнительные сведения см. в документации по GDI.

</dd> <dt>

**хбитмап**
</dt> <dd>

Маркер для точечного рисунка.

</dd> <dt>

**хмаппинг**
</dt> <dd>

Обрабатывает объект сопоставления файлов, используемый для совместного использования памяти между GDI и объектом [**Цимажесампле**](cimagesample.md) .

</dd> <dt>

**pBase**
</dt> <dd>

Адрес точечного рисунка.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl> |



 

 




