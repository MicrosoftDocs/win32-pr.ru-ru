---
description: Дополнительные сведения о перечислении Готосекондариндексбукмаркгрбит
title: Перечисление Готосекондариндексбукмаркгрбит
TOCTitle: GotoSecondaryIndexBookmarkGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.gotosecondaryindexbookmarkgrbit(v=EXCHG.10)
ms:contentKeyID: 39515224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.BookmarkPermitVirtualCurrency
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.BookmarkPermitVirtualCurrency
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f38b5f26abc4dfafb95d5560b3ff1def4267527c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662694"
---
# <a name="gotosecondaryindexbookmarkgrbit-enumeration"></a><span data-ttu-id="a58cc-103">Перечисление Готосекондариндексбукмаркгрбит</span><span class="sxs-lookup"><span data-stu-id="a58cc-103">GotoSecondaryIndexBookmarkGrbit enumeration</span></span>

<span data-ttu-id="a58cc-104">Параметры для [жетготосекондариндексбукмарк (JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] , Int32, готосекондариндексбукмаркгрбит)](./api.jetgotosecondaryindexbookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="a58cc-104">Options for [JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, \[\], Int32, \[\], Int32, GotoSecondaryIndexBookmarkGrbit)](./api.jetgotosecondaryindexbookmark-method.md).</span></span>

<span data-ttu-id="a58cc-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="a58cc-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="a58cc-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a58cc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a58cc-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a58cc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a58cc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a58cc-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GotoSecondaryIndexBookmarkGrbit
'Usage
Dim instance As GotoSecondaryIndexBookmarkGrbit
```

``` csharp
[FlagsAttribute]
public enum GotoSecondaryIndexBookmarkGrbit
```

## <a name="members"></a><span data-ttu-id="a58cc-109">Члены</span><span class="sxs-lookup"><span data-stu-id="a58cc-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="a58cc-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="a58cc-110">Member name</span></span></th>
<th><span data-ttu-id="a58cc-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a58cc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a58cc-112">Нет</span><span class="sxs-lookup"><span data-stu-id="a58cc-112">None</span></span></td>
<td><span data-ttu-id="a58cc-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a58cc-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a58cc-114">букмаркпермитвиртуалкурренци</span><span class="sxs-lookup"><span data-stu-id="a58cc-114">BookmarkPermitVirtualCurrency</span></span></td>
<td><span data-ttu-id="a58cc-115">В случае, если запись индекса больше не может быть найдена, курсор будет расположен слева, где была найдена Эта запись индекса.</span><span class="sxs-lookup"><span data-stu-id="a58cc-115">In the event that the index entry can no longer be found, the cursor will be left positioned where that index entry was previously found.</span></span> <span data-ttu-id="a58cc-116">Операция по-прежнему завершится ошибкой с JET_errRecordDeleted; Тем не менее, можно перейти к следующей или предыдущей записи индекса относительно записи индекса, которая сейчас отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a58cc-116">The operation will still fail with JET_errRecordDeleted; however, it will be possible to move to the next or previous index entry relative to the index entry that is now missing.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="a58cc-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a58cc-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a58cc-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="a58cc-118">Reference</span></span>

[<span data-ttu-id="a58cc-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a58cc-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
