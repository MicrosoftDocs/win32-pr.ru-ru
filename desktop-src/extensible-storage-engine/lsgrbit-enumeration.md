---
description: Дополнительные сведения о перечислении Лсгрбит
title: Перечисление Лсгрбит
TOCTitle: LsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.LsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.lsgrbit(v=EXCHG.10)
ms:contentKeyID: 39514518
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.LsGrbit
- Microsoft.Isam.Esent.Interop.LsGrbit.Cursor
- Microsoft.Isam.Esent.Interop.LsGrbit.None
- Microsoft.Isam.Esent.Interop.LsGrbit.Reset
- Microsoft.Isam.Esent.Interop.LsGrbit.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.LsGrbit
- Microsoft.Isam.Esent.Interop.LsGrbit.Reset
- Microsoft.Isam.Esent.Interop.LsGrbit.None
- Microsoft.Isam.Esent.Interop.LsGrbit.Table
- Microsoft.Isam.Esent.Interop.LsGrbit.Cursor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fc0a60d039d0eb1307558d42a3e7a3c7e99eb86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072813"
---
# <a name="lsgrbit-enumeration"></a><span data-ttu-id="65e89-103">Перечисление Лсгрбит</span><span class="sxs-lookup"><span data-stu-id="65e89-103">LsGrbit enumeration</span></span>

<span data-ttu-id="65e89-104">Параметры для [жетсетлс (JET_SESID, JET_TABLEID, JET_LS, лсгрбит)](./api.jetsetls-method.md) и [жетжетлс (JET_SESID, JET_TABLEID, JET_LS, лсгрбит)](./api.jetgetls-method.md).</span><span class="sxs-lookup"><span data-stu-id="65e89-104">Options for [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md) and [JetGetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md).</span></span>

<span data-ttu-id="65e89-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="65e89-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="65e89-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="65e89-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="65e89-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="65e89-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="65e89-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65e89-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration LsGrbit
'Usage
Dim instance As LsGrbit
```

``` csharp
[FlagsAttribute]
public enum LsGrbit
```

## <a name="members"></a><span data-ttu-id="65e89-109">Члены</span><span class="sxs-lookup"><span data-stu-id="65e89-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="65e89-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="65e89-110">Member name</span></span></th>
<th><span data-ttu-id="65e89-111">Описание</span><span class="sxs-lookup"><span data-stu-id="65e89-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="65e89-112">Нет</span><span class="sxs-lookup"><span data-stu-id="65e89-112">None</span></span></td>
<td><span data-ttu-id="65e89-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="65e89-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="65e89-114">Reset</span><span class="sxs-lookup"><span data-stu-id="65e89-114">Reset</span></span></td>
<td><span data-ttu-id="65e89-115">Обработчик контекста для выбранного объекта должен быть сброшен в JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="65e89-115">The context handle for the chosen object should be reset to JET_LSNil.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="65e89-116">Курсор</span><span class="sxs-lookup"><span data-stu-id="65e89-116">Cursor</span></span></td>
<td><span data-ttu-id="65e89-117">Указывает, что маркер контекста должен быть связан с данным курсором.</span><span class="sxs-lookup"><span data-stu-id="65e89-117">Specifies the context handle should be associated with the given cursor.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="65e89-118">Таблица</span><span class="sxs-lookup"><span data-stu-id="65e89-118">Table</span></span></td>
<td><span data-ttu-id="65e89-119">Указывает, что маркер контекста должен быть связан с таблицей, связанной с данным курсором.</span><span class="sxs-lookup"><span data-stu-id="65e89-119">Specifies that the context handle should be associated with the table associated with the given cursor.</span></span> <span data-ttu-id="65e89-120">Использование этого параметра с курсором недопустимо.</span><span class="sxs-lookup"><span data-stu-id="65e89-120">It is illegal to use this option with Cursor.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="65e89-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65e89-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="65e89-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="65e89-122">Reference</span></span>

[<span data-ttu-id="65e89-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="65e89-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
