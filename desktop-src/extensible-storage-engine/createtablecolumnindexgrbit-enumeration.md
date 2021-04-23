---
description: Дополнительные сведения о перечислении Креатетаблеколумниндексгрбит
title: Перечисление Креатетаблеколумниндексгрбит
TOCTitle: CreateTableColumnIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createtablecolumnindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39516657
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72f91c5d41b8262e3b2804159914b0a9ccaaaa7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999545"
---
# <a name="createtablecolumnindexgrbit-enumeration"></a><span data-ttu-id="6a262-103">Перечисление Креатетаблеколумниндексгрбит</span><span class="sxs-lookup"><span data-stu-id="6a262-103">CreateTableColumnIndexGrbit enumeration</span></span>

<span data-ttu-id="6a262-104">Параметры для Жеткреатетаблеколумниндекс.</span><span class="sxs-lookup"><span data-stu-id="6a262-104">Options for JetCreateTableColumnIndex.</span></span>

<span data-ttu-id="6a262-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="6a262-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="6a262-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6a262-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6a262-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6a262-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6a262-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a262-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateTableColumnIndexGrbit
'Usage
Dim instance As CreateTableColumnIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateTableColumnIndexGrbit
```

## <a name="members"></a><span data-ttu-id="6a262-109">Члены</span><span class="sxs-lookup"><span data-stu-id="6a262-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="6a262-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="6a262-110">Member name</span></span></th>
<th><span data-ttu-id="6a262-111">Описание</span><span class="sxs-lookup"><span data-stu-id="6a262-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="6a262-112">Нет</span><span class="sxs-lookup"><span data-stu-id="6a262-112">None</span></span></td>
<td><span data-ttu-id="6a262-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6a262-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="6a262-114">фикседддл</span><span class="sxs-lookup"><span data-stu-id="6a262-114">FixedDDL</span></span></td>
<td><span data-ttu-id="6a262-115">DDL является фиксированным.</span><span class="sxs-lookup"><span data-stu-id="6a262-115">The DDL is fixed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="6a262-116">темплатетабле</span><span class="sxs-lookup"><span data-stu-id="6a262-116">TemplateTable</span></span></td>
<td><span data-ttu-id="6a262-117">Язык DDL наследуется.</span><span class="sxs-lookup"><span data-stu-id="6a262-117">The DDL is inheritable.</span></span> <span data-ttu-id="6a262-118">Подразумевает Фикседддл.</span><span class="sxs-lookup"><span data-stu-id="6a262-118">Implies FixedDDL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="6a262-119">нофикседварколумнсиндериведтаблес</span><span class="sxs-lookup"><span data-stu-id="6a262-119">NoFixedVarColumnsInDerivedTables</span></span></td>
<td><span data-ttu-id="6a262-120">Используется в сочетании с Темплатетабле.</span><span class="sxs-lookup"><span data-stu-id="6a262-120">Used in conjunction with TemplateTable.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="6a262-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a262-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6a262-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="6a262-122">Reference</span></span>

[<span data-ttu-id="6a262-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6a262-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
