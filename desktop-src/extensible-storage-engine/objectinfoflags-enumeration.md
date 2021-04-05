---
description: Дополнительные сведения о перечислении Обжектинфофлагс
title: Перечисление Обжектинфофлагс
TOCTitle: ObjectInfoFlags enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfoflags(v=EXCHG.10)
ms:contentKeyID: 39515824
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3f301f1e786d126dbd57c071fe89356e0acc891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910240"
---
# <a name="objectinfoflags-enumeration"></a><span data-ttu-id="f8222-103">Перечисление Обжектинфофлагс</span><span class="sxs-lookup"><span data-stu-id="f8222-103">ObjectInfoFlags enumeration</span></span>

<span data-ttu-id="f8222-104">Флаги для объектов ESENT (таблиц).</span><span class="sxs-lookup"><span data-stu-id="f8222-104">Flags for ESENT objects (tables).</span></span> <span data-ttu-id="f8222-105">Используется в [JET_OBJECTINFO](./jet-objectinfo-class.md).</span><span class="sxs-lookup"><span data-stu-id="f8222-105">Used in [JET_OBJECTINFO](./jet-objectinfo-class.md).</span></span>

<span data-ttu-id="f8222-106">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="f8222-106">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="f8222-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8222-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f8222-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f8222-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8222-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8222-109">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoFlags
'Usage
Dim instance As ObjectInfoFlags
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoFlags
```

## <a name="members"></a><span data-ttu-id="f8222-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f8222-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f8222-111">Имя участника</span><span class="sxs-lookup"><span data-stu-id="f8222-111">Member name</span></span></th>
<th><span data-ttu-id="f8222-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f8222-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f8222-113">Нет</span><span class="sxs-lookup"><span data-stu-id="f8222-113">None</span></span></td>
<td><span data-ttu-id="f8222-114">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8222-114">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f8222-115">Система</span><span class="sxs-lookup"><span data-stu-id="f8222-115">System</span></span></td>
<td><span data-ttu-id="f8222-116">Объект предназначен только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="f8222-116">Object is for internal use only.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f8222-117">таблефикседддл</span><span class="sxs-lookup"><span data-stu-id="f8222-117">TableFixedDDL</span></span></td>
<td><span data-ttu-id="f8222-118">Таблица DDL таблицы исправлена.</span><span class="sxs-lookup"><span data-stu-id="f8222-118">Table's DDL is fixed.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f8222-119">таблетемплате</span><span class="sxs-lookup"><span data-stu-id="f8222-119">TableTemplate</span></span></td>
<td><span data-ttu-id="f8222-120">DDL таблицы является наследуемым.</span><span class="sxs-lookup"><span data-stu-id="f8222-120">Table's DDL is inheritable.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f8222-121">табледеривед</span><span class="sxs-lookup"><span data-stu-id="f8222-121">TableDerived</span></span></td>
<td><span data-ttu-id="f8222-122">DDL таблицы наследуется из таблицы шаблонов.</span><span class="sxs-lookup"><span data-stu-id="f8222-122">Table's DDL is inherited from a template table.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f8222-123">табленофикседварколумнсиндериведтаблес</span><span class="sxs-lookup"><span data-stu-id="f8222-123">TableNoFixedVarColumnsInDerivedTables</span></span></td>
<td><span data-ttu-id="f8222-124">Фиксированные или переменные столбцы в производных таблицах (чтобы в будущем можно было добавить в шаблон фиксированные или переменные столбцы).</span><span class="sxs-lookup"><span data-stu-id="f8222-124">Fixed or variable columns in derived tables (so that fixed or variable columns can be added to the template in the future).</span></span> <span data-ttu-id="f8222-125">Используется в сочетании с Таблетемплате.</span><span class="sxs-lookup"><span data-stu-id="f8222-125">Used in conjunction with TableTemplate.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f8222-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8222-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8222-127">Справочник</span><span class="sxs-lookup"><span data-stu-id="f8222-127">Reference</span></span>

[<span data-ttu-id="f8222-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f8222-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
