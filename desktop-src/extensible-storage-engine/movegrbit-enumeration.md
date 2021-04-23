---
description: Дополнительные сведения о перечислении Мовегрбит
title: Перечисление Мовегрбит
TOCTitle: MoveGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MoveGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.movegrbit(v=EXCHG.10)
ms:contentKeyID: 39513771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MoveGrbit
- Microsoft.Isam.Esent.Interop.MoveGrbit.MoveKeyNE
- Microsoft.Isam.Esent.Interop.MoveGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MoveGrbit
- Microsoft.Isam.Esent.Interop.MoveGrbit.None
- Microsoft.Isam.Esent.Interop.MoveGrbit.MoveKeyNE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81f047cd69bca668a5eae2b5147d8c0a137011e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080879"
---
# <a name="movegrbit-enumeration"></a><span data-ttu-id="ab370-103">Перечисление Мовегрбит</span><span class="sxs-lookup"><span data-stu-id="ab370-103">MoveGrbit enumeration</span></span>

<span data-ttu-id="ab370-104">Параметры для Жетмове.</span><span class="sxs-lookup"><span data-stu-id="ab370-104">Options for JetMove.</span></span>

<span data-ttu-id="ab370-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="ab370-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="ab370-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ab370-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ab370-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ab370-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ab370-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab370-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MoveGrbit
'Usage
Dim instance As MoveGrbit
```

``` csharp
[FlagsAttribute]
public enum MoveGrbit
```

## <a name="members"></a><span data-ttu-id="ab370-109">Члены</span><span class="sxs-lookup"><span data-stu-id="ab370-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ab370-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="ab370-110">Member name</span></span></th>
<th><span data-ttu-id="ab370-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ab370-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ab370-112">Нет</span><span class="sxs-lookup"><span data-stu-id="ab370-112">None</span></span></td>
<td><span data-ttu-id="ab370-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab370-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ab370-114">мовекэйне</span><span class="sxs-lookup"><span data-stu-id="ab370-114">MoveKeyNE</span></span></td>
<td><span data-ttu-id="ab370-115">Перемещает курсор вперед или назад по количеству записей индекса, необходимых для пропуска запрошенного количества значений ключа индекса, обнаруженных в индексе.</span><span class="sxs-lookup"><span data-stu-id="ab370-115">Moves the cursor forward or backward by the number of index entries required to skip the requested number of index key values encountered in the index.</span></span> <span data-ttu-id="ab370-116">Это влияет на свертывание записей индекса с повторяющимися значениями ключа в одну запись индекса.</span><span class="sxs-lookup"><span data-stu-id="ab370-116">This has the effect of collapsing index entries with duplicate key values into a single index entry.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ab370-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab370-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ab370-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="ab370-118">Reference</span></span>

[<span data-ttu-id="ab370-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ab370-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
