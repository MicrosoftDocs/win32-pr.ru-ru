---
description: Дополнительные сведения о перечислении Спацехинтсгрбит
title: Перечисление Спацехинтсгрбит
TOCTitle: SpaceHintsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SpaceHintsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.spacehintsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516304
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.CreateHintHotpointSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.CreateHintAppendSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.DeleteHintTableSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.None
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve2
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve1
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintTableScanForward
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintTableScanBackward
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve3
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.SpaceHintUtilizeParentSpace
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve3
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.CreateHintHotpointSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.CreateHintAppendSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintTableScanBackward
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.SpaceHintUtilizeParentSpace
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve2
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.DeleteHintTableSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintTableScanForward
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.None
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8a2ee172355b48e64f62f2b18477373269d81ae060460ad34ff45dbad33a91b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978534"
---
# <a name="spacehintsgrbit-enumeration"></a>Перечисление Спацехинтсгрбит

Параметры для [JET_SPACEHINTS](./jet-spacehints-class.md).

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SpaceHintsGrbit
'Usage
Dim instance As SpaceHintsGrbit
```

``` csharp
[FlagsAttribute]
public enum SpaceHintsGrbit
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
<td>спацехинтутилизепарентспаце</td>
<td>При этом внутренняя политика выделения будет изменена таким образом, чтобы пространство было в иерархическом порядке от непосредственного родителя сбалансированного дерева.</td>
</tr>
<tr class="odd">
<td></td>
<td>креатехинтаппендсекуентиал</td>
<td>Этот бит позволяет расширить режим разбиения на части в соответствии с Dynamics of таблицы (задается Кбминекстент, Улгровс, Кбмаксекстент).</td>
</tr>
<tr class="even">
<td></td>
<td>креатехинсотпоинтсекуентиал</td>
<td>Этот бит обеспечит рост поведения Хотпоинт Split в соответствии с Dynamics of таблицы (устанавливается параметрами Кбминекстент, Улгровс, Кбмаксекстент).</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveHintReserve1</td>
<td>Зарезервировано и игнорируется.</td>
</tr>
<tr class="even">
<td></td>
<td>ретриевехинттаблесканфорвард</td>
<td>Если задать этот параметр, клиент указывает на то, что перенаправление последовательного просмотра — это основная модель использования этой таблицы.</td>
</tr>
<tr class="odd">
<td></td>
<td>ретриевехинттаблесканбакквард</td>
<td>Если задать этот параметр, клиент указывает на то, что при обратной последовательной проверке используется основная схема использования этой таблицы.</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveHintReserve2</td>
<td>Зарезервировано и игнорируется.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveHintReserve3</td>
<td>Зарезервировано и игнорируется.</td>
</tr>
<tr class="even">
<td></td>
<td>делетехинттаблесекуентиал</td>
<td>Приложение ждет, чтобы эта таблица была очищена последовательно (от наименьшего ключа к максимальному).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
