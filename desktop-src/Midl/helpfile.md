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
ms.openlocfilehash: 1557d96f35913e5e1ed9b784bedfc430e6c4d77b65954583ca6923e4728af9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384026"
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

## <a name="remarks"></a>Remarks

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

[**Библиотечная**](library.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 