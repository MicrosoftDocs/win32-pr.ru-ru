---
description: 'Дополнительные сведения: JET_DBID'
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c576734a3e2da71f041509e5b7d7d9244427dbb8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986697"
---
# <a name="jet_dbid"></a>JET_DBID


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_dbid"></a>JET_DBID

Тип данных **JET_DBID** содержит обработчик для базы данных. Для управления схемой базы данных используется маркер базы данных. Его также можно использовать для управления таблицами в этой базе данных.

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a>Типы данных

JET_DBID

Обработчик для базы данных.

Значение JET_dbidNil указывает, что маркер является недопустимым.

### <a name="remarks"></a>Комментарии

Маркер базы данных создается с помощью вызова [жеткреатедатабасе](./jetcreatedatabase-function.md) или [жетопендатабасе](./jetopendatabase-function.md).

Маркер базы данных может быть явно закрыт [жетклоседатабасе](./jetclosedatabase-function.md) или неявно закрыт [жетендсессион](./jetendsession-function.md) или [жеттерм](./jetterm-function.md).

Маркер базы данных может использоваться только в том сеансе, в котором он был создан. Наличие маркера базы данных соответствует логическому открытию базы данных. Логическое открытие отличается от физического открытия базы данных, что происходит при присоединении базы данных к системе.

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[жеткреатедатабасе](./jetcreatedatabase-function.md)  
[жетопендатабасе](./jetopendatabase-function.md)  
[жетклоседатабасе](./jetclosedatabase-function.md)  
[жетендсессион](./jetendsession-function.md)
