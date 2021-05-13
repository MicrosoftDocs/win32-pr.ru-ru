---
description: Содержит сведения, используемые диспетчером файлов для добавления строки справки для элемента меню или команды панели инструментов.
title: Структура FMS_HELPSTRING (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b3ae7f86-5d58-47fa-87bd-e4e6a3541a93
ms.openlocfilehash: 4e9521df91619d108c7a03b6574926147fc2b04a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842215"
---
# <a name="fms_helpstring-structure"></a>\_Структура FMS HELPSTRING

Содержит сведения, используемые диспетчером файлов для добавления строки справки для элемента меню или команды панели инструментов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a>Члены

<dl> <dt>

**идкомманд**
</dt> <dd>

Тип: **int**

</dd> <dd>

Идентификатор элемента команды.

</dd> <dt>

**hMenu**
</dt> <dd>

Тип: **HMENU**

</dd> <dd>

Идентификатор строки меню.

</dd> <dt>

**сзелп**
</dt> <dd>

Тип: **\_ \_ WCHAR \_ t \[ 128 \]**

</dd> <dd>

Строка, завершающаяся нулем, которая получает текст справки.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Вфекст. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**фмекстенсионпрок**](fmextensionproc.md)
</dt> <dt>

[**ФМЕВЕНТ \_ хелпменуитем**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




