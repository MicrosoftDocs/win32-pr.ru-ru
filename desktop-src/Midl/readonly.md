---
title: readonly - атрибут
description: Атрибут \ ReadOnly \ запрещает Присваивание переменной.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- атрибут ReadOnly MIDL
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987461"
---
# <a name="readonly-attribute"></a>readonly - атрибут

Атрибут **\[ ReadOnly \]** запрещает Присваивание переменной.

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*необязательные атрибуты* 
</dt> <dd>

Ноль или несколько атрибутов MIDL.

</dd> <dt>

*тип данных* 
</dt> <dd>

Тип данных, содержащихся в *идентификаторе*.

</dd> <dt>

*identifier* 
</dt> <dd>

Имя, по которому программное обеспечение может ссылаться на место хранения данных.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Атрибут **\[ ReadOnly \]** запрещает Присваивание переменной. **\[ ReadOnly \]** поддерживается только на уровне параметров, а не на уровне метода.

### <a name="flags"></a>Флаги

ВАРФЛАГ \_ фреадонли

## <a name="examples"></a>Примеры

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
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

 

 