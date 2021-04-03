---
title: helpfile - атрибут
description: Атрибут \ HelpFile \ задает имя файла справки для библиотеки типов. Все типы в библиотеке совместно используют один и тот же файл справки.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- атрибут HelpFile MIDL
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b4283b0285631a710af774d364a01b82c9d44b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790021"
---
# <a name="helpfile-attribute"></a>helpfile - атрибут

Атрибут **\[ HelpFile \]** задает имя файла справки для библиотеки типов. Все типы в библиотеке совместно используют один и тот же файл справки.

``` syntax
[
    uuid(uuid-number), 
    helpfile("filename") 
    [, optional-attribute-list]
] 
library 
{
    library statements
};
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*UUID — номер* 
</dt> <dd>

Задает универсальный уникальный идентификационный номер для [**библиотеки**](library.md).

</dd> <dt>

*filename* 
</dt> <dd>

Указывает имя файла, содержащего текст справки.

</dd> <dt>

*список необязательных атрибутов* 
</dt> <dd>

Указывает ноль или более атрибутов, которые компилятор MIDL будет применять к [**библиотеке**](library.md).

</dd> <dt>

*библиотечные операторы* 
</dt> <dd>

Задает одну или несколько инструкций MIDL, определяющих интерфейс библиотеки.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для получения имени файла используйте функции **Кодокумента** в интерфейсах **ITypeLib** и **ITypeInfo** .

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpfile("filename.hlp"),
    lcid(0x0409), 
    version(2.0)
]
library Hello
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**библиотека**](library.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 