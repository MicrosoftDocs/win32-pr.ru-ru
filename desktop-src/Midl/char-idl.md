---
title: char, атрибут
description: Ключевое слово char определяет 8-разрядный элемент данных.
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- атрибут char MIDL
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889828"
---
# <a name="char-attribute"></a>char, атрибут

Ключевое слово **char** определяет 8-разрядный элемент данных.

``` syntax
char identifier-name;
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор — имя* 
</dt> <dd>

Указывает допустимый идентификатор MIDL. Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Ключевое слово **char** определяет элемент данных с 8 битами. Для компилятора MIDL **символ** по умолчанию не подписан и является синонимом [**неподписанного**](unsigned.md) **char**.

В этой версии Microsoft RPC таблицы преобразования символов, выполняющие преобразование между ASCII и EBCDIC, встроены в библиотеки времени выполнения и не могут быть изменены пользователем.

Тип **char** является одним из базовых типов языка определения интерфейса (IDL). Тип **char** может отображаться в виде спецификатора типа в объявлениях [**const**](const.md) , объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в виде спецификатора возвращаемого типа функции и описателя типа параметра). Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).

Компиляторы DCE IDL не принимают ключевое слово, [**Подписывание**](signed.md) которого было применено к типам **char** . Поэтому эта функция недоступна при использовании параметра компилятора MIDL [**/ОСФ**](-osf.md) .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Базовые типы MIDL](midl-base-types.md)
</dt> <dt>

[**byte**](byte.md)
</dt> <dt>

[**/Char**](-char.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/осф**](-osf.md)
</dt> <dt>

[**входил**](signed.md)
</dt> <dt>

[**Строка**](string.md)
</dt> <dt>

[**определение**](typedef.md)
</dt> <dt>

[**без знака**](unsigned.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




