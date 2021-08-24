---
description: Структура ПРОПЕРТИНСТ определяет экземпляр свойства в части распознаваемых данных. Сетевой монитор выделяет и заполняет структуру ПРОПЕРТИНСТ, когда свойство прикрепляется к записи.
ms.assetid: d8382a38-b634-4c65-b56b-44fee067a0fe
title: Структура ПРОПЕРТИНСТ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINST
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0d1c338fb8b4e63f03bff422e25578132476f70d932e8f17d5b0c39a0f6416e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778504"
---
# <a name="propertyinst-structure"></a>Структура ПРОПЕРТИНСТ

Структура **пропертинст** определяет экземпляр свойства в части распознаваемых данных. Сетевой монитор выделяет и заполняет структуру **пропертинст** , когда свойство прикрепляется к записи.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PROPERTYINST {
  LPPROPERTYINFO lpPropertyInfo;
  LPSTR          szPropertyText;
  union {
    LPVOID           lpData;
    ULPBYTE          lpByte;
    ULPWORD          lpWord;
    ULPDWORD         lpDword;
    ULPLARGEINT      lpLargeInt;
    ULPSYSTEMTIME    lpSysTime;
    LPPROPERTYINSTEX lpPropertyInstEx;
  };
  WORD           DataLength;
  WORD           Level  :4;
  WORD           HelpID  :12;
  DWORD          IFlags;
} PROPERTYINST, *LPPROPERTYINST;
```



## <a name="members"></a>Члены

<dl> <dt>

**лппропертинфо**
</dt> <dd>

Указатель на структуру [PROPERTYINFO](propertyinfo.md) , определяющую свойство.

</dd> <dt>

**сзпропертитекст**
</dt> <dd>

Указатель на строку, которая отображается в области сведений пользовательского интерфейса сетевой монитор.

</dd> <dt>

**лпдата**
</dt> <dd>

Указатель на начало данных для свойства. Средство синтаксического анализа определяет, откуда запускаются данные свойства.

</dd> <dt>

**lpByte**
</dt> <dd>

Указатель на **байтовые** данные.

</dd> <dt>

**лпворд**
</dt> <dd>

Указатель на данные **слова** .

</dd> <dt>

**лпдворд**
</dt> <dd>

Указатель на данные **DWORD** .

</dd> <dt>

**лпларжеинт**
</dt> <dd>

Указатель на данные [**ларжеинт**](largeint.md) .

</dd> <dt>

**лпсистиме**
</dt> <dd>

Указатель на данные [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .

</dd> <dt>

**лппропертинстекс**
</dt> <dd>

Указатель на структуру [пропертинстекс](propertyinstex.md) . Элемент **лппропертинстекс** используется только при вызове [аттачпропертинстанцеекс](attachpropertyinstanceex.md).

Если используется **лппропертинстекс** , необходимо задать для элемента **DATALENGTH** значение 0xFFFF.

</dd> <dt>

**DataLength**
</dt> <dd>

Длина данных для этого экземпляра свойства. Если элемент **лппропертинстекс** указывает на структуру [**пропертинстекс**](propertyinstex.md) , необходимо установить параметр **DATALENGTH** в значение 0xFFFF.

</dd> <dt>

**Уровень**
</dt> <dd>

Сведения об уровне.

</dd> <dt>

**Идентификатор справки**
</dt> <dd>

Идентификатор контекста файла справки.

</dd> <dt>

**ифлагс**
</dt> <dd>

Флаг условия ошибки.

</dd> </dl>

## <a name="remarks"></a>Remarks

Структура **пропертинст** определяет экземпляр присоединенного свойства. Средство синтаксического анализа обращается к структуре **пропертинст** через несколько вспомогательных функций. Например, при вызове функции [**форматпропертинстанце**](formatpropertyinstance.md) для форматирования данных свойства он изменяет элемент **сзпропертитекст** структуры **пропертинст** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[аттачпропертинстанце](attachpropertyinstance.md)
</dt> <dt>

[аттачпропертинстанцеекс](attachpropertyinstanceex.md)
</dt> </dl>

 

