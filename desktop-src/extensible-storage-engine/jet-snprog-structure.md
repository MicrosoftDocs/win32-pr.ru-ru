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
ms.openlocfilehash: 961e9cf264652924cfb1d870fa1a04aabc7fb61a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496953"
---
# <a name="jet_snprog-structure"></a>Структура JET_SNPROG


_**Применимо к:** Windows | Windows Server_

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
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>

