---
description: Дополнительные сведения о перечислении Бегинтрансактионгрбит
title: Перечисление Бегинтрансактионгрбит
TOCTitle: BeginTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.begintransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39515115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5f407c54b7b6e76ab63dcfb97d1307458ba15277
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816984"
---
# <a name="begintransactiongrbit-enumeration"></a><span data-ttu-id="ab1e7-103">Перечисление Бегинтрансактионгрбит</span><span class="sxs-lookup"><span data-stu-id="ab1e7-103">BeginTransactionGrbit enumeration</span></span>

<span data-ttu-id="ab1e7-104">Параметры для [JetBeginTransaction2 (JET_SESID, бегинтрансактионгрбит)](./api.jetbegintransaction2-method.md).</span><span class="sxs-lookup"><span data-stu-id="ab1e7-104">Options for [JetBeginTransaction2(JET_SESID, BeginTransactionGrbit)](./api.jetbegintransaction2-method.md).</span></span>

<span data-ttu-id="ab1e7-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="ab1e7-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="ab1e7-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ab1e7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ab1e7-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ab1e7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ab1e7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab1e7-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginTransactionGrbit
'Usage
Dim instance As BeginTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="ab1e7-109">Члены</span><span class="sxs-lookup"><span data-stu-id="ab1e7-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ab1e7-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="ab1e7-110">Member name</span></span></th>
<th><span data-ttu-id="ab1e7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ab1e7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ab1e7-112">Нет</span><span class="sxs-lookup"><span data-stu-id="ab1e7-112">None</span></span></td>
<td><span data-ttu-id="ab1e7-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab1e7-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ab1e7-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ab1e7-114">ReadOnly</span></span></td>
<td><span data-ttu-id="ab1e7-115">Транзакция не изменит базу данных.</span><span class="sxs-lookup"><span data-stu-id="ab1e7-115">The transaction will not modify the database.</span></span> <span data-ttu-id="ab1e7-116">При попытке обновления эта операция завершится ошибкой с параметром <a href="hh564840(v=exchg.10).md">ReadOnly</a>.</span><span class="sxs-lookup"><span data-stu-id="ab1e7-116">If an update is attempted, that operation will fail with <a href="hh564840(v=exchg.10).md">TransReadOnly</a>.</span></span> <span data-ttu-id="ab1e7-117">Этот параметр игнорируется, если он не запрашивается, если данный сеанс еще не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="ab1e7-117">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ab1e7-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab1e7-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ab1e7-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="ab1e7-119">Reference</span></span>

[<span data-ttu-id="ab1e7-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ab1e7-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
