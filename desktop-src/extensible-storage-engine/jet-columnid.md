---
description: 'Дополнительные сведения: JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
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
ms.openlocfilehash: fbdc03342187cfc2adfa1dcd3ed650f532e1dbc0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982947"
---
# <a name="jet_columnid"></a>JET_COLUMNID


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_columnid"></a>JET_COLUMNID

Тип данных **JET_COLUMNID** определяет столбец в таблице.

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a>Типы данных

JET_COLUMNID

Определяет столбец в таблице.

### <a name="remarks"></a>Комментарии

Идентификаторы столбцов уникальны в пределах одной таблицы. Когда известно, что столбец имеет определенный идентификатор столбца, он всегда будет иметь идентификатор столбца. При восстановлении из резервной копии не изменится значение идентификатора столбца. Однако при удалении одного или нескольких столбцов таблицы, предшествовавших определенному столбцу таблицы, база данных Compact может изменить значение идентификатора столбца.

В некоторых случаях идентификаторы столбцов являются единственным средством идентификации столбцов. При создании временной таблицы ее столбцы не имеют имен, но массив идентификаторов столбцов возвращается функцией Create.

Столбцы в разных таблицах могут иметь один и тот же идентификатор столбца.

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 


