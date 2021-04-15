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
ms.openlocfilehash: 87590013ef905ffbdd13dd3b767435a907b08783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676001"
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
| Header<br/> | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl> |



 

 




