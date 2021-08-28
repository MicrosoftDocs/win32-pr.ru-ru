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
ms.openlocfilehash: d898a5943b5b80e738a331971595995d0fdee4eb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482300"
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


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 


