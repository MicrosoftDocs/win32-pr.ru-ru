---
description: 'Дополнительные сведения: JET_PSTR'
title: JET_PSTR
TOCTitle: JET_PSTR
ms:assetid: acb1143f-a5ee-4088-9f05-cc2aeef23442
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294056(v=EXCHG.10)
ms:contentKeyID: 32765667
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
ms.openlocfilehash: 442af61595f8bfdd81d0d36d0d8687f0e0418761
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986097"
---
# <a name="jet_pstr"></a>JET_PSTR


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_pstr"></a>JET_PSTR

Тип данных JET_PSTR содержит строку ASCII, завершающуюся нулем (char \* ).

**Windows vista: JET_PSTR** введены в Windows vista.

```cpp
    typedef __nullterminated char *  JET_PSTR;
```

### <a name="data-types"></a>Типы данных

JET_PSTR

Строка ASCII, заканчивающаяся символом NULL \* .

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 


