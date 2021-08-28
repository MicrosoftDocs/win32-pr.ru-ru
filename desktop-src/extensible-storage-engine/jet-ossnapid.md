---
description: 'Дополнительные сведения: JET_OSSNAPID'
title: JET_OSSNAPID
TOCTitle: JET_OSSNAPID
ms:assetid: 89b15492-674a-46e4-8aea-991df4f22a6f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269325(v=EXCHG.10)
ms:contentKeyID: 32765615
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
ms.openlocfilehash: 82be9a4aa00f1880493d81dbcd53d1d8d76cc46a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983807"
---
# <a name="jet_ossnapid"></a>JET_OSSNAPID


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_ossnapid"></a>JET_OSSNAPID

**JET_OSSNAPID** тип данных содержит маркер моментального снимка базы данных.

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a>Типы данных

JET_OSSNAPID

Маркер моментального снимка базы данных. Этот маркер используется в элементах API JET, которые участвуют в резервном копировании моментальных снимков.

**Null** можно использовать для указания недопустимого маркера.

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 


