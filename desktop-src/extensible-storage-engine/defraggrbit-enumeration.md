---
description: Дополнительные сведения о перечислении Дефраггрбит
title: Перечисление Дефраггрбит
TOCTitle: DefragGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DefragGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.defraggrbit(v=EXCHG.10)
ms:contentKeyID: 39516122
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5da047fbdad20ac40d780dc5b0bba9e986e7672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713195"
---
# <a name="defraggrbit-enumeration"></a><span data-ttu-id="e6d8c-103">Перечисление Дефраггрбит</span><span class="sxs-lookup"><span data-stu-id="e6d8c-103">DefragGrbit enumeration</span></span>

<span data-ttu-id="e6d8c-104">Параметры для [жетдефрагмент (JET_SESID, JET_DBID, String, Int32, Int32, дефраггрбит)](./api.jetdefragment-method.md).</span><span class="sxs-lookup"><span data-stu-id="e6d8c-104">Options for [JetDefragment(JET_SESID, JET_DBID, String, Int32, Int32, DefragGrbit)](./api.jetdefragment-method.md).</span></span>

<span data-ttu-id="e6d8c-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="e6d8c-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="e6d8c-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e6d8c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e6d8c-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e6d8c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d8c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6d8c-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DefragGrbit
'Usage
Dim instance As DefragGrbit
```

``` csharp
[FlagsAttribute]
public enum DefragGrbit
```

## <a name="members"></a><span data-ttu-id="e6d8c-109">Члены</span><span class="sxs-lookup"><span data-stu-id="e6d8c-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e6d8c-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="e6d8c-110">Member name</span></span></th>
<th><span data-ttu-id="e6d8c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e6d8c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e6d8c-112">аваилспацетрисонли</span><span class="sxs-lookup"><span data-stu-id="e6d8c-112">AvailSpaceTreesOnly</span></span></td>
<td><span data-ttu-id="e6d8c-113">Дефрагментация доступного места в выделенном пространстве базы данных ESE.</span><span class="sxs-lookup"><span data-stu-id="e6d8c-113">Defragments the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="e6d8c-114">Пространство базы данных делится на два типа: пространство и доступное пространство.</span><span class="sxs-lookup"><span data-stu-id="e6d8c-114">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="e6d8c-115">Владельцем пространства выделяется таблица или индекс, в то время как доступное место может быть готово к использованию в таблице или индексе соответственно.</span><span class="sxs-lookup"><span data-stu-id="e6d8c-115">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="e6d8c-116">Доступное пространство является гораздо более динамичным в поведении и требует дополнительной дефрагментации, что больше, чем принадлежащие пространства или данные таблицы или индекса.</span><span class="sxs-lookup"><span data-stu-id="e6d8c-116">Available space is much more dynamic in behavior and requires on-line defragmentation more so than owned space or table or index data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e6d8c-117">батчстарт</span><span class="sxs-lookup"><span data-stu-id="e6d8c-117">BatchStart</span></span></td>
<td><span data-ttu-id="e6d8c-118">Запускает новую задачу дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="e6d8c-118">Starts a new defragmentation task.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e6d8c-119">батчстоп</span><span class="sxs-lookup"><span data-stu-id="e6d8c-119">BatchStop</span></span></td>
<td><span data-ttu-id="e6d8c-120">Останавливает задачу дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="e6d8c-120">Stops a defragmentation task.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="e6d8c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6d8c-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6d8c-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="e6d8c-122">Reference</span></span>

[<span data-ttu-id="e6d8c-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e6d8c-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
