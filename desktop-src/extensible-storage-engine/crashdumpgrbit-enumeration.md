---
description: Дополнительные сведения о перечислении Крашдумпгрбит
title: Перечисление Крашдумпгрбит (Microsoft. ISAM. ESENT. Interop. Windows7)
TOCTitle: CrashDumpGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.crashdumpgrbit(v=EXCHG.10)
ms:contentKeyID: 39515535
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCachedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMinimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Maximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCorruptedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMaximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeDirtyPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Minimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeDirtyPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMaximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMinimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCachedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCorruptedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Minimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Maximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cad58cac50d42b7abaadb179b4068bda2534383113b48430c79d874357c030c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118083488"
---
# <a name="crashdumpgrbit-enumeration"></a>Перечисление Крашдумпгрбит

Параметры для Жетконфигурепроцессфоркрашдумп.

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CrashDumpGrbit
'Usage
Dim instance As CrashDumpGrbit
```

``` csharp
[FlagsAttribute]
public enum CrashDumpGrbit
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
<td>Минимум</td>
<td>Дамп минимум включает Качеминимум.</td>
</tr>
<tr class="odd">
<td></td>
<td>Максимум</td>
<td>Максимальный размер дампа включает Качемаксимум.</td>
</tr>
<tr class="even">
<td></td>
<td>качеминимум</td>
<td>Качеминимум включает кратковременные страницы. Качеминимум включает страницы, используемые для памяти. Качеминимум включает страницы, помеченные ошибками.</td>
</tr>
<tr class="odd">
<td></td>
<td>качемаксимум</td>
<td>Максимальный размер кэша включает минимум кэша. Максимальный размер кэша включает весь образ кэша.</td>
</tr>
<tr class="even">
<td></td>
<td>качеинклудедиртипажес</td>
<td>Дамп включает измененные страницы.</td>
</tr>
<tr class="odd">
<td></td>
<td>качеинклудекачедпажес</td>
<td>Дамп включает страницы, содержащие допустимые данные.</td>
</tr>
<tr class="even">
<td></td>
<td>качеинклудекорруптедпажес</td>
<td>Дамп включает поврежденные страницы (ресурсоемкие для вычислений).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)
