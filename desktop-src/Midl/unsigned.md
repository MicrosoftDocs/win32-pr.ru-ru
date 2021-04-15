---
title: неподписанный атрибут
description: Ключевое слово без знака указывает, что наиболее значимый бит целочисленной переменной представляет бит данных, а не бит со знаком.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- неподписанный атрибут MIDL
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329d638f1b5be97e5b441aa4e84825fe59a4a3f0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105661665"
---
# <a name="unsigned-attribute"></a>неподписанный атрибут

Ключевое слово **без знака** указывает, что наиболее значимый бит целочисленной переменной представляет бит данных, а не бит со знаком.

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Может быть любым из типов [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**int**](int.md), [**Short**](short.md)и [**Small**](small.md).

</dd> <dt>

*идентификатор — имя* 
</dt> <dd>

Указывает допустимый идентификатор MIDL. Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это ключевое слово является необязательным и может использоваться с любыми символьными и целочисленными типами [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)и [**Small**](small.md). При необходимости можно включить ключевое слово [**int**](int.md) после квалификаторов типа **Long**, **Short** и **Small**.

При использовании параметра компилятора MIDL [**/char**](-char.md)типы символов и целых чисел, отображаемые в IDL-файле без явных ключевых слов Sign, могут отображаться с ключевым словом [**со знаком**](signed.md) или **без знака** в создаваемом файле заголовка. Чтобы избежать путаницы, укажите знак целого числа и символьных типов.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Базовые типы MIDL](midl-base-types.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**/Char**](-char.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**поддерживаем**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**входил**](signed.md)
</dt> <dt>

[**значительные**](small.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




