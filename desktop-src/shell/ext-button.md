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
ms.openlocfilehash: 6d1505ef7b330f0e935136eacaf808da3add8cd8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843155"
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



## <a name="members"></a>Члены

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

## <a name="requirements"></a>Requirements (Требования)



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

 

 




