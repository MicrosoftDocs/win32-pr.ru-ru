---
description: Дополнительные сведения о перечислении Термгрбит
title: Перечисление Термгрбит
TOCTitle: TermGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TermGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.termgrbit(v=EXCHG.10)
ms:contentKeyID: 39511147
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TermGrbit.None
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 49b466b298a78d7bfd6822904aed977e7117b927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817137"
---
# <a name="termgrbit-enumeration"></a><span data-ttu-id="2367f-103">Перечисление Термгрбит</span><span class="sxs-lookup"><span data-stu-id="2367f-103">TermGrbit enumeration</span></span>

<span data-ttu-id="2367f-104">Параметры для [JetTerm2 (JET_INSTANCE, термгрбит)](./api.jetterm2-method.md).</span><span class="sxs-lookup"><span data-stu-id="2367f-104">Options for [JetTerm2(JET_INSTANCE, TermGrbit)](./api.jetterm2-method.md).</span></span>

<span data-ttu-id="2367f-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="2367f-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="2367f-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2367f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2367f-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2367f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2367f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2367f-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TermGrbit
'Usage
Dim instance As TermGrbit
```

``` csharp
[FlagsAttribute]
public enum TermGrbit
```

## <a name="members"></a><span data-ttu-id="2367f-109">Члены</span><span class="sxs-lookup"><span data-stu-id="2367f-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="2367f-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="2367f-110">Member name</span></span></th>
<th><span data-ttu-id="2367f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2367f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2367f-112">Нет</span><span class="sxs-lookup"><span data-stu-id="2367f-112">None</span></span></td>
<td><span data-ttu-id="2367f-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2367f-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2367f-114">Завершить</span><span class="sxs-lookup"><span data-stu-id="2367f-114">Complete</span></span></td>
<td><span data-ttu-id="2367f-115">Запрашивает корректное завершение работы экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2367f-115">Requests that the instance be shut down cleanly.</span></span> <span data-ttu-id="2367f-116">Все необязательные операции по очистке, обычно выполняемые в фоновом режиме во время выполнения, выполняются немедленно.</span><span class="sxs-lookup"><span data-stu-id="2367f-116">Any optional cleanup work that would ordinarily be done in the background at run time is completed immediately.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2367f-117">Аварийного</span><span class="sxs-lookup"><span data-stu-id="2367f-117">Abrupt</span></span></td>
<td><span data-ttu-id="2367f-118">Запрашивает как можно быстрее завершить работу экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2367f-118">Requests that the instance be shut down as quickly as possible.</span></span> <span data-ttu-id="2367f-119">Все необязательные операции, которые обычно выполняются в фоновом режиме во время выполнения, прекращаются.</span><span class="sxs-lookup"><span data-stu-id="2367f-119">Any optional work that would ordinarily be done in the background at run time is abandoned.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="2367f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2367f-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2367f-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="2367f-121">Reference</span></span>

[<span data-ttu-id="2367f-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2367f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="2367f-123">Бит</span><span class="sxs-lookup"><span data-stu-id="2367f-123">Dirty</span></span>](./windows7grbits.dirty-field.md)
