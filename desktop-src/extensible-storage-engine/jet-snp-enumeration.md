---
description: 'Дополнительные сведения: перечисление JET_SNP'
title: Перечисление JET_SNP
TOCTitle: JET_SNP enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNP
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snp(v=EXCHG.10)
ms:contentKeyID: 39511218
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10061d0c00d90aa5ca4e0778cba046d2e6f62f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692132"
---
# <a name="jet_snp-enumeration"></a><span data-ttu-id="66387-103">Перечисление JET_SNP</span><span class="sxs-lookup"><span data-stu-id="66387-103">JET_SNP enumeration</span></span>

<span data-ttu-id="66387-104">Тип операции, для которой сообщается ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="66387-104">The type of operation that progress is being reported for.</span></span>

<span data-ttu-id="66387-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="66387-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="66387-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="66387-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="66387-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66387-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_SNP
'Usage
Dim instance As JET_SNP
```

``` csharp
public enum JET_SNP
```

## <a name="members"></a><span data-ttu-id="66387-108">Члены</span><span class="sxs-lookup"><span data-stu-id="66387-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="66387-109">Имя участника</span><span class="sxs-lookup"><span data-stu-id="66387-109">Member name</span></span></th>
<th><span data-ttu-id="66387-110">Описание</span><span class="sxs-lookup"><span data-stu-id="66387-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="66387-111">Восстановить</span><span class="sxs-lookup"><span data-stu-id="66387-111">Repair</span></span></td>
<td><span data-ttu-id="66387-112">Обратный вызов для параметра восстановления.</span><span class="sxs-lookup"><span data-stu-id="66387-112">Callback is for a repair option.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="66387-113">Компактный</span><span class="sxs-lookup"><span data-stu-id="66387-113">Compact</span></span></td>
<td><span data-ttu-id="66387-114">Обратный вызов для дефрагментации базы данных.</span><span class="sxs-lookup"><span data-stu-id="66387-114">Callback is for database defragmentation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="66387-115">Восстановить</span><span class="sxs-lookup"><span data-stu-id="66387-115">Restore</span></span></td>
<td><span data-ttu-id="66387-116">Обратный вызов для параметров восстановления.</span><span class="sxs-lookup"><span data-stu-id="66387-116">Callback is for a restore options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="66387-117">Резервное копирование</span><span class="sxs-lookup"><span data-stu-id="66387-117">Backup</span></span></td>
<td><span data-ttu-id="66387-118">Обратный вызов для параметров резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="66387-118">Callback is for a backup options.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="66387-119">Ведите</span><span class="sxs-lookup"><span data-stu-id="66387-119">Scrub</span></span></td>
<td><span data-ttu-id="66387-120">Обратный вызов для обнуления базы данных.</span><span class="sxs-lookup"><span data-stu-id="66387-120">Callback is for database zeroing.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="66387-121">упградерекордформат</span><span class="sxs-lookup"><span data-stu-id="66387-121">UpgradeRecordFormat</span></span></td>
<td><span data-ttu-id="66387-122">Обратный вызов для процесса обновления формата записи всех страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="66387-122">Callback is for the process of upgrading the record format of all database pages.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="66387-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66387-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="66387-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="66387-124">Reference</span></span>

[<span data-ttu-id="66387-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="66387-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
