---
description: Дополнительные сведения о перечислении Обжектинфогрбит
title: Перечисление Обжектинфогрбит
TOCTitle: ObjectInfoGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfogrbit(v=EXCHG.10)
ms:contentKeyID: 39516208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4028a2a337b32394029960e45bb0e485c2b6b705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712065"
---
# <a name="objectinfogrbit-enumeration"></a><span data-ttu-id="e423a-103">Перечисление Обжектинфогрбит</span><span class="sxs-lookup"><span data-stu-id="e423a-103">ObjectInfoGrbit enumeration</span></span>

<span data-ttu-id="e423a-104">Параметры таблицы, используемые в [JET_OBJECTINFO](./jet-objectinfo-class.md).</span><span class="sxs-lookup"><span data-stu-id="e423a-104">Table options, used in [JET_OBJECTINFO](./jet-objectinfo-class.md).</span></span>

<span data-ttu-id="e423a-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="e423a-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="e423a-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e423a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e423a-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e423a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e423a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e423a-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoGrbit
'Usage
Dim instance As ObjectInfoGrbit
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoGrbit
```

## <a name="members"></a><span data-ttu-id="e423a-109">Члены</span><span class="sxs-lookup"><span data-stu-id="e423a-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e423a-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="e423a-110">Member name</span></span></th>
<th><span data-ttu-id="e423a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e423a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e423a-112">Закладка</span><span class="sxs-lookup"><span data-stu-id="e423a-112">Bookmark</span></span></td>
<td><span data-ttu-id="e423a-113">В таблице могут быть закладки.</span><span class="sxs-lookup"><span data-stu-id="e423a-113">The table can have bookmarks.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e423a-114">Откат</span><span class="sxs-lookup"><span data-stu-id="e423a-114">Rollback</span></span></td>
<td><span data-ttu-id="e423a-115">Можно выполнить откат таблицы.</span><span class="sxs-lookup"><span data-stu-id="e423a-115">The table can be rolled back.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e423a-116">Обновляется</span><span class="sxs-lookup"><span data-stu-id="e423a-116">Updatable</span></span></td>
<td><span data-ttu-id="e423a-117">Таблицу можно обновить.</span><span class="sxs-lookup"><span data-stu-id="e423a-117">The table can be updated.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="e423a-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e423a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e423a-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="e423a-119">Reference</span></span>

[<span data-ttu-id="e423a-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e423a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
