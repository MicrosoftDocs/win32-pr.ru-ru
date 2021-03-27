---
description: Содержит сведения о кнопке, которая добавляется БИБЛИОТЕКой расширения диспетчера файлов на панель инструментов диспетчера файлов.
title: Структура EXT_BUTTON (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXT_BUTTON
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8cd29a06-0f38-4285-9092-647a391b72d7
ms.openlocfilehash: 5eabb9f5e958b1e0bd15a6412dfbfa276d23f255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809412"
---
# <a name="ext_button-structure"></a>\_Структура кнопки ext

Содержит сведения о кнопке, которая добавляется БИБЛИОТЕКой расширения диспетчера файлов на панель инструментов диспетчера файлов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a>Участники

<dl> <dt>

**идкомманд**
</dt> <dd>

Тип: **слово**

</dd> <dd>

Идентификатор команды для кнопки.

</dd> <dt>

**идшелп**
</dt> <dd>

Тип: **слово**

</dd> <dd>

Идентификатор строки справки для кнопки.

</dd> <dt>

**фсстиле**
</dt> <dd>

Тип: **слово**

</dd> <dd>

Стиль кнопки.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Вфекст. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ФМЕВЕНТ \_ тулбарлоад**](fmevent-toolbarload.md)
</dt> <dt>

[**FMS \_ тулбарлоад**](fms-toolbarload.md)
</dt> </dl>

 

 




