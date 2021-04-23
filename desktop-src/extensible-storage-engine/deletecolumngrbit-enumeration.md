---
description: Дополнительные сведения о перечислении Делетеколумнгрбит
title: Перечисление Делетеколумнгрбит
TOCTitle: DeleteColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.deletecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39512792
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.IgnoreTemplateColumns
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.None
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.IgnoreTemplateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3191d3c73883d0bd27b4944718f2a0b3423e2c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719400"
---
# <a name="deletecolumngrbit-enumeration"></a><span data-ttu-id="2a300-103">Перечисление Делетеколумнгрбит</span><span class="sxs-lookup"><span data-stu-id="2a300-103">DeleteColumnGrbit enumeration</span></span>

<span data-ttu-id="2a300-104">Параметры для [JetDeleteColumn2 (JET_SESID, JET_TABLEID, String, делетеколумнгрбит)](./api.jetdeletecolumn2-method.md).</span><span class="sxs-lookup"><span data-stu-id="2a300-104">Options for [JetDeleteColumn2(JET_SESID, JET_TABLEID, String, DeleteColumnGrbit)](./api.jetdeletecolumn2-method.md).</span></span>

<span data-ttu-id="2a300-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="2a300-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="2a300-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2a300-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2a300-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2a300-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2a300-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a300-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DeleteColumnGrbit
'Usage
Dim instance As DeleteColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum DeleteColumnGrbit
```

## <a name="members"></a><span data-ttu-id="2a300-109">Члены</span><span class="sxs-lookup"><span data-stu-id="2a300-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="2a300-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="2a300-110">Member name</span></span></th>
<th><span data-ttu-id="2a300-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2a300-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2a300-112">Нет</span><span class="sxs-lookup"><span data-stu-id="2a300-112">None</span></span></td>
<td><span data-ttu-id="2a300-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a300-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2a300-114">игноретемплатеколумнс</span><span class="sxs-lookup"><span data-stu-id="2a300-114">IgnoreTemplateColumns</span></span></td>
<td><span data-ttu-id="2a300-115">API должен попытаться удалить только столбцы из производной таблицы.</span><span class="sxs-lookup"><span data-stu-id="2a300-115">The API should only attempt to delete columns in the derived table.</span></span> <span data-ttu-id="2a300-116">Если столбец с таким именем существует в базовой таблице, он будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="2a300-116">If a column of that name exists in the base table it will be ignored.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="2a300-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a300-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2a300-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="2a300-118">Reference</span></span>

[<span data-ttu-id="2a300-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2a300-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
