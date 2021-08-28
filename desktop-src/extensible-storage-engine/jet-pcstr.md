---
description: 'Дополнительные сведения: JET_PCSTR'
title: JET_PCSTR
TOCTitle: JET_PCSTR
ms:assetid: 5826e6b9-5297-421f-abaa-016708bf16f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269254(v=EXCHG.10)
ms:contentKeyID: 32765556
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
ms.openlocfilehash: 9ed32b23f99ad9e19d5384bfab1f81ff5ee6a181
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478470"
---
# <a name="jet_pcstr"></a>JET_PCSTR


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_pcstr"></a>JET_PCSTR

Тип данных **JET_PCSTR** содержит константную строку **ASCII** с завершающим нулем (символ \* ).

**Windows vista: JET_PCSTR** введены в Windows vista.

```cpp
    typedef __nullterminated const char *  JET_PCSTR;
```

### <a name="data-types"></a>Типы данных

JET_PCSTR

Строка константы ASCII с завершающим нулем (символ \* ).

### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 


