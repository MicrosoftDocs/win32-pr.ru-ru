---
description: 'Дополнительные сведения: JET_PWSTR'
title: JET_PWSTR
TOCTitle: JET_PWSTR
ms:assetid: 6575f0f0-d022-4e70-9f17-c1d884d9e226
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269271(v=EXCHG.10)
ms:contentKeyID: 32765573
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
ms.openlocfilehash: ca4478684e79dfb698dd30bb21132f597129fdac
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479340"
---
# <a name="jet_pwstr"></a>JET_PWSTR


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_pwstr"></a>JET_PWSTR

Тип данных **JET_PWSTR** содержит строку в **Юникоде** , заканчивающуюся символом NULL \* .

**Windows vista: JET_PWSTR** введены в Windows vista.

```cpp
    typedef __nullterminated WCHAR * JET_PWSTR;
```

### <a name="data-types"></a>Типы данных

JET_PWSTR

Заканчивающийся нулем, строка в Юникоде (char \* ).

### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 


