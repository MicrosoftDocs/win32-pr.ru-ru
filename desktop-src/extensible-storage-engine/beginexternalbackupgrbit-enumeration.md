---
description: Дополнительные сведения о перечислении Бегинекстерналбаккупгрбит
title: Перечисление Бегинекстерналбаккупгрбит
TOCTitle: BeginExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.beginexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39509773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b68cbfc75d0a71eacedb4bbd462fcd8a93d43690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674321"
---
# <a name="beginexternalbackupgrbit-enumeration"></a><span data-ttu-id="5dee6-103">Перечисление Бегинекстерналбаккупгрбит</span><span class="sxs-lookup"><span data-stu-id="5dee6-103">BeginExternalBackupGrbit enumeration</span></span>

<span data-ttu-id="5dee6-104">Параметры для [жетбегинекстерналбаккупинстанце (JET_INSTANCE, бегинекстерналбаккупгрбит)](./api.jetbeginexternalbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="5dee6-104">Options for [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md).</span></span>

<span data-ttu-id="5dee6-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="5dee6-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="5dee6-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5dee6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5dee6-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5dee6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5dee6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dee6-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginExternalBackupGrbit
'Usage
Dim instance As BeginExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginExternalBackupGrbit
```

## <a name="members"></a><span data-ttu-id="5dee6-109">Члены</span><span class="sxs-lookup"><span data-stu-id="5dee6-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="5dee6-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="5dee6-110">Member name</span></span></th>
<th><span data-ttu-id="5dee6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="5dee6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="5dee6-112">Нет</span><span class="sxs-lookup"><span data-stu-id="5dee6-112">None</span></span></td>
<td><span data-ttu-id="5dee6-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5dee6-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="5dee6-114">Добавочный</span><span class="sxs-lookup"><span data-stu-id="5dee6-114">Incremental</span></span></td>
<td><span data-ttu-id="5dee6-115">Создает добавочное резервное копирование, а не полное резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="5dee6-115">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="5dee6-116">Это означает, что резервное копирование выполняется только для файлов журнала с момента последнего полного или добавочного резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="5dee6-116">This means that only the log files since the last full or incremental backup will be backed up.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="5dee6-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dee6-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5dee6-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="5dee6-118">Reference</span></span>

[<span data-ttu-id="5dee6-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5dee6-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
