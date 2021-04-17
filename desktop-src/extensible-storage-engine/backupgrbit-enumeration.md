---
description: Дополнительные сведения о перечислении Баккупгрбит
title: Перечисление Баккупгрбит
TOCTitle: BackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.backupgrbit(v=EXCHG.10)
ms:contentKeyID: 39512196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bda9754efcae8ebe353b8272ba57c5640ecdf946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674323"
---
# <a name="backupgrbit-enumeration"></a><span data-ttu-id="bbe4d-103">Перечисление Баккупгрбит</span><span class="sxs-lookup"><span data-stu-id="bbe4d-103">BackupGrbit enumeration</span></span>

<span data-ttu-id="bbe4d-104">Параметры для [жетбаккупинстанце (JET_INSTANCE, String, баккупгрбит, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="bbe4d-104">Options for [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span></span>

<span data-ttu-id="bbe4d-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="bbe4d-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="bbe4d-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bbe4d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bbe4d-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bbe4d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe4d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbe4d-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BackupGrbit
'Usage
Dim instance As BackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BackupGrbit
```

## <a name="members"></a><span data-ttu-id="bbe4d-109">Члены</span><span class="sxs-lookup"><span data-stu-id="bbe4d-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="bbe4d-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="bbe4d-110">Member name</span></span></th>
<th><span data-ttu-id="bbe4d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="bbe4d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="bbe4d-112">Нет</span><span class="sxs-lookup"><span data-stu-id="bbe4d-112">None</span></span></td>
<td><span data-ttu-id="bbe4d-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bbe4d-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="bbe4d-114">Добавочный</span><span class="sxs-lookup"><span data-stu-id="bbe4d-114">Incremental</span></span></td>
<td><span data-ttu-id="bbe4d-115">Создает добавочное резервное копирование, а не полное резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="bbe4d-115">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="bbe4d-116">Это означает, что резервное копирование выполняется только для файлов журнала, созданных с момента последнего полного или добавочного резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="bbe4d-116">This means that only the log files created since the last full or incremental backup will be backed up.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="bbe4d-117">At</span><span class="sxs-lookup"><span data-stu-id="bbe4d-117">Atomic</span></span></td>
<td><span data-ttu-id="bbe4d-118">Создает полную резервную копию базы данных.</span><span class="sxs-lookup"><span data-stu-id="bbe4d-118">Creates a full backup of the database.</span></span> <span data-ttu-id="bbe4d-119">Это позволяет сохранять существующую резервную копию в том же каталоге в случае сбоя новой резервной копии.</span><span class="sxs-lookup"><span data-stu-id="bbe4d-119">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="bbe4d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbe4d-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bbe4d-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="bbe4d-121">Reference</span></span>

[<span data-ttu-id="bbe4d-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bbe4d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
