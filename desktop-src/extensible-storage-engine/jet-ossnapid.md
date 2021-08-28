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
ms.openlocfilehash: d6185f17c16cbdb2a45e172a14af346c3519aa12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468371"
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


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 


