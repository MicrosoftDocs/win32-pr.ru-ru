---
description: 'Дополнительные сведения: JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
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
ms.openlocfilehash: 35120be9a26dcbdc8d012cd12c871ddcf8f71555
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105714059"
---
# <a name="jet_err"></a>JET_ERR


_**Применимо к:** Windows | Windows Server_

## <a name="jet_err"></a>JET_ERR

Тип данных **JET_ERR** содержит [Расширенный код ошибки подсистемы хранилища](./extensible-storage-engine-error-codes.md).

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a>Типы данных

JET_ERR

Нулевое значение (соответствующее JET_errSuccess) указывает на Успешный вызов. Положительное значение предупреждает о некритическом условии, произошедшем при успешном вызове по ошибке. Отрицательное значение указывает на сбой вызова.

### <a name="remarks"></a>Комментарии

Сведения об возврате ошибок в виде значений HRESULT см. в разделе [ошибки расширенного подсистемы хранилища](./extensible-storage-engine-errors.md). Дополнительные сведения о флагах настройки базы данных для обработки ошибок см. в разделе [Параметры обработки ошибок](./error-handling-parameters.md).

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


### <a name="see-also"></a>См. также:

[Ошибки расширяемого подсистемы хранилища](./extensible-storage-engine-errors.md)  
[Коды ошибок расширенного подсистемы хранилища](./extensible-storage-engine-error-codes.md)  
[Параметры обработки ошибок](./error-handling-parameters.md)
