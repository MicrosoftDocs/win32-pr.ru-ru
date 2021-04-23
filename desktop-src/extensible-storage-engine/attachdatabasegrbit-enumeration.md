---
description: Дополнительные сведения о перечислении Аттачдатабасегрбит
title: Перечисление Аттачдатабасегрбит
TOCTitle: AttachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.attachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514410
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81525e97f1b6266ba15baab50168404566bd7bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674415"
---
# <a name="attachdatabasegrbit-enumeration"></a><span data-ttu-id="71ddf-103">Перечисление Аттачдатабасегрбит</span><span class="sxs-lookup"><span data-stu-id="71ddf-103">AttachDatabaseGrbit enumeration</span></span>

<span data-ttu-id="71ddf-104">Параметры для Жетаттачдатабасе.</span><span class="sxs-lookup"><span data-stu-id="71ddf-104">Options for JetAttachDatabase.</span></span>

<span data-ttu-id="71ddf-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="71ddf-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="71ddf-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="71ddf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="71ddf-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="71ddf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="71ddf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71ddf-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration AttachDatabaseGrbit
'Usage
Dim instance As AttachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum AttachDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="71ddf-109">Члены</span><span class="sxs-lookup"><span data-stu-id="71ddf-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="71ddf-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="71ddf-110">Member name</span></span></th>
<th><span data-ttu-id="71ddf-111">Описание</span><span class="sxs-lookup"><span data-stu-id="71ddf-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="71ddf-112">Нет</span><span class="sxs-lookup"><span data-stu-id="71ddf-112">None</span></span></td>
<td><span data-ttu-id="71ddf-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71ddf-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="71ddf-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="71ddf-114">ReadOnly</span></span></td>
<td><span data-ttu-id="71ddf-115">Предотвращает изменения в базе данных.</span><span class="sxs-lookup"><span data-stu-id="71ddf-115">Prevents modifications to the database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="71ddf-116">делетекорруптиндексес</span><span class="sxs-lookup"><span data-stu-id="71ddf-116">DeleteCorruptIndexes</span></span></td>
<td><span data-ttu-id="71ddf-117">Если параметр JET_paramEnableIndexChecking установлен, все индексы данных в Юникоде будут удалены.</span><span class="sxs-lookup"><span data-stu-id="71ddf-117">If JET_paramEnableIndexChecking has been set, all indexes over Unicode data will be deleted.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="71ddf-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71ddf-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="71ddf-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="71ddf-119">Reference</span></span>

[<span data-ttu-id="71ddf-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="71ddf-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
