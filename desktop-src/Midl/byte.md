---
title: Byte, атрибут
description: Ключевое слово byte задает 8-разрядный элемент данных.
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- байтовый атрибут MIDL
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a271cc81fe97fb25850bfe4dcb7d2edb55ba3c69805dab17d013bc646768e87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384733"
---
# <a name="byte-attribute"></a>Byte, атрибут

Ключевое слово **Byte** задает 8-разрядный элемент данных.

``` syntax
byte identifier-name;
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор — имя* 
</dt> <dd>

Указывает допустимый идентификатор MIDL. Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.

</dd> </dl>

## <a name="remarks"></a>Remarks

Элемент данных в **байтах** не преобразуется для передачи в сети в качестве типа [**char**](char-idl.md) .

Тип **Byte** является одним из базовых типов языка определения интерфейса (IDL). Тип **Byte** может отображаться в виде спецификатора типа в объявлениях [**const**](const.md) , объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в виде спецификатора типа "функция-возврат" и спецификатора типа параметра). Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Базовые типы MIDL](midl-base-types.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Файл определения интерфейса (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**определение**](typedef.md)
</dt> </dl>

 

 




