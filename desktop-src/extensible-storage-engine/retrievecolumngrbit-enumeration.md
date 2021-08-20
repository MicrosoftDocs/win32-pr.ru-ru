---
description: Дополнительные сведения о перечислении Ретриевеколумнгрбит
title: Перечисление Ретриевеколумнгрбит
TOCTitle: RetrieveColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.retrievecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39511391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7bd59f610b2ff1423b82539c61eff3d9d770a03d6f8291a1bae53b372fff318f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890672"
---
# <a name="retrievecolumngrbit-enumeration"></a>Перечисление Ретриевеколумнгрбит

Параметры для Жетретриевеколумн.

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RetrieveColumnGrbit
'Usage
Dim instance As RetrieveColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum RetrieveColumnGrbit
```

## <a name="members"></a>Члены

<table>
<thead>
<tr class="header">
<th></th>
<th>Имя участника</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Нет</td>
<td>Параметры по умолчанию.</td>
</tr>
<tr class="even">
<td></td>
<td>ретриевекопи</td>
<td>Этот флаг заставляет столбец извлечь измененное значение, а не исходное значение. Если значение не было изменено, то извлекается исходное значение. Таким образом, значение, которое еще не было вставлено или Обновлено, может быть получено во время операции вставки или обновления записи.</td>
</tr>
<tr class="odd">
<td></td>
<td>ретриевефроминдекс</td>
<td>Этот параметр используется для извлечения значений столбцов из индекса, если это возможно, без обращения к записи. Таким образом, необязательная Загрузка записей может быть продолжена, если нужные данные будут доступны из самих записей индекса.</td>
</tr>
<tr class="even">
<td></td>
<td>ретриевефромпримарибукмарк</td>
<td>Этот параметр используется для извлечения значений столбцов из закладки индекса и может отличаться от значения индекса, если столбец отображается как в первичном, так и в текущем индексе. Этот параметр не следует указывать, если текущий индекс является кластеризованным или первичным индексом. Этот бит не может быть установлен, если также задан параметр Ретриевефроминдекс.</td>
</tr>
<tr class="odd">
<td></td>
<td>ретриеветаг</td>
<td>Этот параметр используется для получения порядкового номера значения столбца с несколькими значениями в JET_RETINFO. Итагсекуенце. Получение порядкового номера может быть дорогостоящей операцией, и ее следует выполнять только при необходимости.</td>
</tr>
<tr class="even">
<td></td>
<td>ретриевенулл</td>
<td>Этот параметр используется для извлечения значений NULL в столбцах с несколькими значениями. Если этот параметр не указан, значения NULL в столбцах с несколькими значениями будут пропускаться автоматически.</td>
</tr>
<tr class="odd">
<td></td>
<td>ретриевеигноредефаулт</td>
<td>Этот параметр влияет только на столбцы с несколькими значениями и приводит к возвращению значения NULL, если запрошенный порядковый номер равен 1, а значения для столбца в записи не заданы.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
