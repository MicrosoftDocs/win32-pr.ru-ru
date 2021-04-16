---
title: requestedit - атрибут
description: Атрибут \ рекуестедит \ указывает, что свойство поддерживает уведомление уведомление OnRequestEdit.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- атрибут рекуестедит MIDL
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d83beea34f008e6e96fcd493d8410d7d2c5b88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650328"
---
# <a name="requestedit-attribute"></a>requestedit - атрибут

Атрибут **\[ рекуестедит \]** указывает, что свойство поддерживает уведомление **уведомление OnRequestEdit** .

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*необязательные атрибуты* 
</dt> <dd>

Ноль или несколько атрибутов MIDL.

</dd> <dt>

*Тип возвращаемого значения* 
</dt> <dd>

Указывает тип возвращаемого значения функции.

</dd> <dt>

*имя функции* 
</dt> <dd>

Указывает имя функции в IDL-файле.

</dd> <dt>

*params* 
</dt> <dd>

Ноль или более параметров функции.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Поддержка **уведомление OnRequestEdit** уведомления означает, что перед внесением изменений объект отправляет клиенту запрос на изменение свойства. Объект может поддерживать привязку данных, но не имеет этого атрибута.

### <a name="flags"></a>Флаги

ФУНКФЛАГ \_ фрекуестедит, варфлаг \_ фрекуестедит

## <a name="examples"></a>Примеры

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 