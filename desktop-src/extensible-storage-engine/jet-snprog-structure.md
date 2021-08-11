---
description: 'Дополнительные сведения: структура JET_SNPROG'
title: Структура JET_SNPROG
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 251f7948ec4d15e455720043b847abbd855e24146dd05a432b2bf3ea6d28dfef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118252771"
---
# <a name="jet_snprog-structure"></a>Структура JET_SNPROG


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_snprog-structure"></a>Структура JET_SNPROG

Структура **JET_SNPROG** содержит сведения о ходе выполнения длительной операции. Когда вызывается функция обратного вызова для уведомления о состоянии операции, и операция все еще выполняется, последний параметр функции обратного вызова является указателем на структуру **JET_SNPROG** .

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер структуры **JET_SNPROG** в байтах. Это значение подтверждает наличие следующих полей.

**кунитдоне**

Количество рабочих единиц, уже выполненных во время выполнения длительной функции.

**куниттотал**

Количество единиц работы, которые необходимо выполнить. Это значение всегда должно быть больше или равно **кунитдоне**.

### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>

