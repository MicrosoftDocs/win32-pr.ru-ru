---
description: Дополнительные сведения о перечислении Ресизедатабасегрбит
title: Перечисление Ресизедатабасегрбит (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: ResizeDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.resizedatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 55104329
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.OnlyGrow
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.OnlyGrow
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51d703f96882136e2b88f1a2df37609573c725e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683583"
---
# <a name="resizedatabasegrbit-enumeration"></a><span data-ttu-id="1354a-103">Перечисление Ресизедатабасегрбит</span><span class="sxs-lookup"><span data-stu-id="1354a-103">ResizeDatabaseGrbit enumeration</span></span>

<span data-ttu-id="1354a-104">Параметры для [жетресизедатабасе (JET_SESID, JET_DBID, Int32, Int32, ресизедатабасегрбит)](./windows8api.jetresizedatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="1354a-104">Options for [JetResizeDatabase(JET_SESID, JET_DBID, Int32, Int32, ResizeDatabaseGrbit)](./windows8api.jetresizedatabase-method.md).</span></span>

<span data-ttu-id="1354a-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="1354a-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="1354a-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1354a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="1354a-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1354a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1354a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1354a-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ResizeDatabaseGrbit
'Usage
Dim instance As ResizeDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum ResizeDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="1354a-109">Члены</span><span class="sxs-lookup"><span data-stu-id="1354a-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="1354a-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="1354a-110">Member name</span></span></th>
<th><span data-ttu-id="1354a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1354a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1354a-112">Нет</span><span class="sxs-lookup"><span data-stu-id="1354a-112">None</span></span></td>
<td><span data-ttu-id="1354a-113">Без параметра.</span><span class="sxs-lookup"><span data-stu-id="1354a-113">No option.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1354a-114">онлигров</span><span class="sxs-lookup"><span data-stu-id="1354a-114">OnlyGrow</span></span></td>
<td><span data-ttu-id="1354a-115">Увеличивать только базу данных.</span><span class="sxs-lookup"><span data-stu-id="1354a-115">Only grow the database.</span></span> <span data-ttu-id="1354a-116">Если при вызове изменения размера база данных будет сжата, ничего делать не нужно.</span><span class="sxs-lookup"><span data-stu-id="1354a-116">If the resize call would shrink the database, do nothing.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="1354a-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1354a-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1354a-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="1354a-118">Reference</span></span>

[<span data-ttu-id="1354a-119">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="1354a-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
