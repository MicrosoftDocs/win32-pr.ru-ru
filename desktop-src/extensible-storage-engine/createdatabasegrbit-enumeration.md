---
description: Дополнительные сведения о перечислении Креатедатабасегрбит
title: Перечисление Креатедатабасегрбит
TOCTitle: CreateDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39515634
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e23b7b875863b747fc5d2ba021c90d5f7f71048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080386"
---
# <a name="createdatabasegrbit-enumeration"></a>Перечисление Креатедатабасегрбит

Параметры для [жеткреатедатабасе (JET_SESID, String, String, JET_DBID, креатедатабасегрбит)](./api.jetcreatedatabase-method.md).

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateDatabaseGrbit
'Usage
Dim instance As CreateDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateDatabaseGrbit
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
<td>овервритиксистинг</td>
<td>По умолчанию, если вызывается Жеткреатедатабасе и база данных уже существует, вызов API завершится ошибкой и исходная база данных не будет перезаписана. Овервритиксистинг изменяет это поведение, и старая база данных будет перезаписана новой.</td>
</tr>
<tr class="odd">
<td></td>
<td>рековерйофф</td>
<td>Отключает ведение журнала. Установка этого бита теряет возможность воспроизведения файлов журнала и восстановления базы данных до стабильного работоспособного состояния после сбоя.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
