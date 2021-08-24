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
ms.openlocfilehash: 4d0d534efe8df1f4d05cd0b536a78094f903870d896114ee8b614511e067025b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013682"
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

## <a name="remarks"></a>Remarks

Атрибут **\[ ReadOnly \]** запрещает Присваивание переменной. **\[ ReadOnly \]** поддерживается только на уровне параметров, а не на уровне метода.

### <a name="flags"></a>Флаги

ВАРФЛАГ \_ фреадонли

## <a name="examples"></a>Примеры

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a>См. также

<dl> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 