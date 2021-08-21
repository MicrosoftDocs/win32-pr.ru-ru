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
ms.openlocfilehash: 71e5c60b07c7152cf52d1e2ab68925b181d4b356
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467241"
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


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 


