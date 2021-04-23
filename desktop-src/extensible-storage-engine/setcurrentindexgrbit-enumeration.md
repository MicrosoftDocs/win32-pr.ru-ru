---
description: Дополнительные сведения о перечислении Сеткуррентиндексгрбит
title: Перечисление Сеткуррентиндексгрбит
TOCTitle: SetCurrentIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcurrentindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39515072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2391715332989bf20aae3d0a666c1cef2ce2e135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711225"
---
# <a name="setcurrentindexgrbit-enumeration"></a><span data-ttu-id="15586-103">Перечисление Сеткуррентиндексгрбит</span><span class="sxs-lookup"><span data-stu-id="15586-103">SetCurrentIndexGrbit enumeration</span></span>

<span data-ttu-id="15586-104">Параметры для [JetSetCurrentIndex2 (JET_SESID, JET_TABLEID, String, сеткуррентиндексгрбит)](./api.jetsetcurrentindex2-method.md) и [JetSetCurrentIndex3 (JET_SESID, JET_TABLEID, String, сеткуррентиндексгрбит, Int32)](./api.jetsetcurrentindex3-method.md).</span><span class="sxs-lookup"><span data-stu-id="15586-104">Options for [JetSetCurrentIndex2(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit)](./api.jetsetcurrentindex2-method.md) and [JetSetCurrentIndex3(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit, Int32)](./api.jetsetcurrentindex3-method.md).</span></span>

<span data-ttu-id="15586-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="15586-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="15586-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="15586-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="15586-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="15586-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="15586-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15586-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetCurrentIndexGrbit
'Usage
Dim instance As SetCurrentIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum SetCurrentIndexGrbit
```

## <a name="members"></a><span data-ttu-id="15586-109">Члены</span><span class="sxs-lookup"><span data-stu-id="15586-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="15586-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="15586-110">Member name</span></span></th>
<th><span data-ttu-id="15586-111">Описание</span><span class="sxs-lookup"><span data-stu-id="15586-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="15586-112">Нет</span><span class="sxs-lookup"><span data-stu-id="15586-112">None</span></span></td>
<td><span data-ttu-id="15586-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="15586-113">Default options.</span></span> <span data-ttu-id="15586-114">Это то же самое, что и MoveFirst.</span><span class="sxs-lookup"><span data-stu-id="15586-114">This is the same as MoveFirst.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="15586-115">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="15586-115">MoveFirst</span></span></td>
<td><span data-ttu-id="15586-116">Указывает, что курсор должен располагаться на первой записи указанного индекса.</span><span class="sxs-lookup"><span data-stu-id="15586-116">Indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="15586-117">Если текущий индекс выбран, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="15586-117">If the current index is being selected then this option is ignored.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="15586-118">Не перемещать</span><span class="sxs-lookup"><span data-stu-id="15586-118">NoMove</span></span></td>
<td><span data-ttu-id="15586-119">Указывает, что курсор должен располагаться на записи индекса нового индекса, который соответствует записи, связанной с записью индекса, в текущей позиции курсора по старому индексу.</span><span class="sxs-lookup"><span data-stu-id="15586-119">Indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="15586-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15586-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="15586-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="15586-121">Reference</span></span>

[<span data-ttu-id="15586-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="15586-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
