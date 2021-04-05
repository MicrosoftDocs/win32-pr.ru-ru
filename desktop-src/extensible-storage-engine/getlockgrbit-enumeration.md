---
description: Дополнительные сведения о перечислении Жетлоккгрбит
title: Перечисление Жетлоккгрбит
TOCTitle: GetLockGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetLockGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getlockgrbit(v=EXCHG.10)
ms:contentKeyID: 39512424
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Read
- Microsoft.Isam.Esent.Interop.GetLockGrbit
- Microsoft.Isam.Esent.Interop.GetLockGrbit.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cfcad088fa93d73910a0333d3aca9a700e97996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991434"
---
# <a name="getlockgrbit-enumeration"></a><span data-ttu-id="cea92-103">Перечисление Жетлоккгрбит</span><span class="sxs-lookup"><span data-stu-id="cea92-103">GetLockGrbit enumeration</span></span>

<span data-ttu-id="cea92-104">Параметры для Жетжетлокк.</span><span class="sxs-lookup"><span data-stu-id="cea92-104">Options for JetGetLock.</span></span>

<span data-ttu-id="cea92-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="cea92-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="cea92-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cea92-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cea92-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cea92-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cea92-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cea92-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetLockGrbit
'Usage
Dim instance As GetLockGrbit
```

``` csharp
[FlagsAttribute]
public enum GetLockGrbit
```

## <a name="members"></a><span data-ttu-id="cea92-109">Члены</span><span class="sxs-lookup"><span data-stu-id="cea92-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="cea92-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="cea92-110">Member name</span></span></th>
<th><span data-ttu-id="cea92-111">Описание</span><span class="sxs-lookup"><span data-stu-id="cea92-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="cea92-112">Чтение</span><span class="sxs-lookup"><span data-stu-id="cea92-112">Read</span></span></td>
<td><span data-ttu-id="cea92-113">Получение блокировки чтения для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="cea92-113">Acquire a read lock on the current record.</span></span> <span data-ttu-id="cea92-114">Блокировки чтения несовместимы с блокировками записи, уже удерживаемыми другими сеансами, но совместимы с блокировками чтения, удерживаемыми другими сеансами.</span><span class="sxs-lookup"><span data-stu-id="cea92-114">Read locks are incompatible with write locks already held by other sessions but are compatible with read locks held by other sessions.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="cea92-115">запись</span><span class="sxs-lookup"><span data-stu-id="cea92-115">Write</span></span></td>
<td><span data-ttu-id="cea92-116">Получение блокировки записи для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="cea92-116">Acquire a write lock on the current record.</span></span> <span data-ttu-id="cea92-117">Блокировки записи несовместимы с блокировками записи или чтения, удерживаемыми другими сеансами, но совместимы с блокировками чтения, удерживаемыми в одном сеансе.</span><span class="sxs-lookup"><span data-stu-id="cea92-117">Write locks are not compatible with write or read locks held by other sessions but are compatible with read locks held by the same session.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="cea92-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cea92-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cea92-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="cea92-119">Reference</span></span>

[<span data-ttu-id="cea92-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="cea92-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
