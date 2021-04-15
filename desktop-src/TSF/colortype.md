---
title: Перечисление КОЛОРТИПЕ (Софткбдк. h)
description: Элементы перечисления КОЛОРТИПЕ используются для указания типов цветов, доступных для экранной клавиатуры.
ms.assetid: 63a51f67-d85c-4017-a569-03df164198db
keywords:
- Платформа текстовых служб перечисления КОЛОРТИПЕ
topic_type:
- apiref
api_name:
- COLORTYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28f3b4111973e9676a34c548db566b1c95ac43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661949"
---
# <a name="colortype-enumeration"></a>Перечисление КОЛОРТИПЕ

Элементы перечисления **колортипе** используются для указания типов цветов, доступных для экранной клавиатуры.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagCOLORTYPE { 
  bkcolor         = 0,
  UnSelForeColor  = 1,
  UnSelTextColor  = 2,
  SelForeColor    = 3,
  SelTextColor    = 4,
  Max_color_Type  = 5
} COLORTYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="bkcolor"></span><span id="BKCOLOR"></span>**бкколор**
</dt> <dd>

Цвет фона.

</dd> <dt>

<span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**унселфореколор**
</dt> <dd>

Цвет переднего плана не выбран.

</dd> <dt>

<span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**унселтекстколор**
</dt> <dd>

Цвет невыделенного текста.

</dd> <dt>

<span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**селфореколор**
</dt> <dd>

Выбранный цвет переднего плана.

</dd> <dt>

<span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**селтекстколор**
</dt> <dd>

Цвет выбранного текста.

</dd> <dt>

<span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**Максимальный \_ \_ Тип цвета**
</dt> <dd>

Максимальный тип цвета.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                        |
| Header<br/>                   | <dl> <dt>Софткбдк. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Софткбд. idl</dt> </dl> |



 

 





