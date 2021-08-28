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
ms.openlocfilehash: 6a698afffb415bb4418f46cfe16091ceda03cb59
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985167"
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


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 


