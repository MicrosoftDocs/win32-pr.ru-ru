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
ms.openlocfilehash: 51a894e5d4a09e7535e10a73e1bd118245e5886e0cdbb23b0f0645e588ab4adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146357"
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

## <a name="remarks"></a>Remarks

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

 

 