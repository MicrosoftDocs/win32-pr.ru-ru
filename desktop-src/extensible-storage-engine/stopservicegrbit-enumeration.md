---
description: Дополнительные сведения о перечислении Стопсервицегрбит
title: Перечисление Стопсервицегрбит (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54e54576dfb1023ec4e3bc55ddd198a77f0ddf25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692514"
---
# <a name="stopservicegrbit-enumeration"></a>Перечисление Стопсервицегрбит

Параметры для [JetStopServiceInstance2 (JET_INSTANCE, стопсервицегрбит)](./windows8api.jetstopserviceinstance2-method.md).

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a>Члены

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
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
<td>Все</td>
<td>Останавливает все службы ESE для указанного экземпляра.</td>
</tr>
<tr class="even">
<td></td>
<td>баккграундусертаскс</td>
<td>Останавливает Перезапускаемые клиентские задачи фонового обслуживания (дефрагментацию B + Tree).</td>
</tr>
<tr class="odd">
<td></td>
<td>куиесцекачес</td>
<td>Куиесцес все "грязные" кэши на диск. Асинхронная. Замораживание отменяется, если впоследствии вызывается бит возобновления.</td>
</tr>
<tr class="even">
<td></td>
<td>Возобновить</td>
<td>Возобновляет ранее выданные операции выхода, т. е. &quot; перезапускает службу &quot; . Можно сочетать с грбитс, чтобы возобновить работу конкретных служб, или с параметром 0x0 возобновляет работу всех предыдущих остановленных служб.
<p>Предупреждение. Этот бит можно использовать только для возобновления JET_bitStopServiceBackground и JET_bitStopServiceQuiesceCaches, если вы выполняли JET_bitStopServiceAll или JET_bitStopServiceAPI, попытка использовать JET_bitStopServiceResume завершится ошибкой.</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
