---
description: Дополнительные сведения о перечислении Коммиттрансактионгрбит
title: Перечисление Коммиттрансактионгрбит
TOCTitle: CommitTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.committransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39510830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a93504d688d1eddfcde81ae23c87e62f70e0aab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719751"
---
# <a name="committransactiongrbit-enumeration"></a><span data-ttu-id="01d9f-103">Перечисление Коммиттрансактионгрбит</span><span class="sxs-lookup"><span data-stu-id="01d9f-103">CommitTransactionGrbit enumeration</span></span>

<span data-ttu-id="01d9f-104">Параметры для Жеткоммиттрансактион.</span><span class="sxs-lookup"><span data-stu-id="01d9f-104">Options for JetCommitTransaction.</span></span>

<span data-ttu-id="01d9f-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="01d9f-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="01d9f-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="01d9f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="01d9f-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="01d9f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="01d9f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01d9f-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CommitTransactionGrbit
'Usage
Dim instance As CommitTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum CommitTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="01d9f-109">Члены</span><span class="sxs-lookup"><span data-stu-id="01d9f-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="01d9f-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="01d9f-110">Member name</span></span></th>
<th><span data-ttu-id="01d9f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="01d9f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="01d9f-112">Нет</span><span class="sxs-lookup"><span data-stu-id="01d9f-112">None</span></span></td>
<td><span data-ttu-id="01d9f-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="01d9f-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="01d9f-114">лазифлуш</span><span class="sxs-lookup"><span data-stu-id="01d9f-114">LazyFlush</span></span></td>
<td><span data-ttu-id="01d9f-115">Транзакция фиксируется обычным образом, но этот API не ждет сброса транзакции в файл журнала транзакций перед возвратом вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="01d9f-115">The transaction is committed normally but this Api does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="01d9f-116">Это радикально сокращает продолжительность операции фиксации за счет устойчивости.</span><span class="sxs-lookup"><span data-stu-id="01d9f-116">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="01d9f-117">Любая транзакция, которая не сброшена в журнал до сбоя, будет автоматически прервана во время восстановления после сбоя во время следующего вызова Жетинит.</span><span class="sxs-lookup"><span data-stu-id="01d9f-117">Any transaction that is not flushed to the log before a crash will be automatically aborted during crash recovery during the next call to JetInit.</span></span> <span data-ttu-id="01d9f-118">Если указаны WaitLastLevel0Commit или WaitAllLevel0Commit, этот параметр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="01d9f-118">If WaitLastLevel0Commit or WaitAllLevel0Commit are specified, this option is ignored.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="01d9f-119">WaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="01d9f-119">WaitLastLevel0Commit</span></span></td>
<td><span data-ttu-id="01d9f-120">Если в сеансе ранее зафиксированы транзакции и они еще не были записаны в файл журнала транзакций, они должны быть сброшены немедленно.</span><span class="sxs-lookup"><span data-stu-id="01d9f-120">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="01d9f-121">Этот API будет ожидать, пока транзакции не будут сброшены перед возвратом в вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="01d9f-121">This Api will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="01d9f-122">Это полезно, если приложение ранее зафиксировало несколько транзакций с помощью JET_bitCommitLazyFlush и теперь хочет сбросить все эти транзакции на диск.</span><span class="sxs-lookup"><span data-stu-id="01d9f-122">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span>
<p><span data-ttu-id="01d9f-123">Этот параметр может использоваться, даже если сеанс в данный момент не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="01d9f-123">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="01d9f-124">Этот параметр нельзя использовать в сочетании с любым другим параметром.</span><span class="sxs-lookup"><span data-stu-id="01d9f-124">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="01d9f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01d9f-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="01d9f-126">Справочник</span><span class="sxs-lookup"><span data-stu-id="01d9f-126">Reference</span></span>

[<span data-ttu-id="01d9f-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="01d9f-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
