---
title: атрибут со знаком
description: Ключевое слово с подписью указывает, что наиболее значимый бит целочисленной переменной представляет бит знака, а не бит данных.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- подписанный атрибут MIDL
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f3db15bc46d6d8ab3ec108c648d094ebf706d9286a8c4b0a823fa409e118e3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641341"
---
# <a name="signed-attribute"></a>атрибут со знаком

Ключевое слово с **подписью** указывает, что наиболее значимый бит целочисленной переменной представляет бит знака, а не бит данных.

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*type-qualifier* 
</dt> <dd>

Может быть любой из типов [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)и [**Small**](small.md).

</dd> <dt>

*идентификатор — имя* 
</dt> <dd>

Указывает допустимый идентификатор MIDL. Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это ключевое слово является необязательным и может использоваться с любыми символьными и целочисленными типами [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)и [**Small**](small.md). При необходимости можно включить ключевое слово [**int**](int.md) после квалификаторов типа **Long**, **Short** и **Small**.

При использовании целочисленного параметра компилятора MIDL типы [**char**](char-idl.md), Character и Integer, которые ОТОБРАЖАЮТСЯ в IDL-файле без явных ключевых слов Sign, могут появляться с **подписанными** или [**неподписанными**](unsigned.md) ключевыми словами в создаваемом файле заголовка. Чтобы избежать путаницы, укажите знак целого числа и символьных типов.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Базовые типы MIDL](midl-base-types.md)
</dt> <dt>

[**/Char**](-char.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**значительные**](small.md)
</dt> <dt>

[**без знака**](unsigned.md)
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 




