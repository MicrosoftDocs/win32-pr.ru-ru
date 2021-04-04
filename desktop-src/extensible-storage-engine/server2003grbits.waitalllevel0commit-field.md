---
description: 'Дополнительные сведения о: Server2003Grbits. WaitAllLevel0Commit поле'
title: Поле Server2003Grbits. WaitAllLevel0Commit (Microsoft. ISAM. ESENT. Interop. server2003)
TOCTitle: WaitAllLevel0Commit field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.waitalllevel0commit(v=EXCHG.10)
ms:contentKeyID: 55104104
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.WaitAllLevel0Commit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16390069adf81ead8e819bc5148a88e30900b508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910228"
---
# <a name="server2003grbitswaitalllevel0commit-field"></a><span data-ttu-id="97001-103">Server2003Grbits. WaitAllLevel0Commit, поле</span><span class="sxs-lookup"><span data-stu-id="97001-103">Server2003Grbits.WaitAllLevel0Commit field</span></span>

<span data-ttu-id="97001-104">Все транзакции, ранее зафиксированные любым сеансом, которые еще не были сброшены в файл журнала транзакций, будут сброшены немедленно.</span><span class="sxs-lookup"><span data-stu-id="97001-104">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="97001-105">Этот API будет ожидать, пока транзакции не будут сброшены перед возвратом в вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="97001-105">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="97001-106">Этот параметр может использоваться, даже если сеанс в данный момент не находится в транзакции.</span><span class="sxs-lookup"><span data-stu-id="97001-106">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="97001-107">Этот параметр нельзя использовать в сочетании с любым другим параметром.</span><span class="sxs-lookup"><span data-stu-id="97001-107">This option cannot be used in combination with any other option.</span></span>

<span data-ttu-id="97001-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="97001-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="97001-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="97001-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="97001-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97001-110">Syntax</span></span>

``` vb
'Declaration
Public Const WaitAllLevel0Commit As CommitTransactionGrbit
'Usage
Dim value As CommitTransactionGrbit

value = Server2003Grbits.WaitAllLevel0Commit
```

``` csharp
public const CommitTransactionGrbit WaitAllLevel0Commit
```

## <a name="see-also"></a><span data-ttu-id="97001-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97001-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="97001-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="97001-112">Reference</span></span>

[<span data-ttu-id="97001-113">Класс Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="97001-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="97001-114">Элементы Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="97001-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="97001-115">Пространство имен Microsoft. ISAM. ESENT. Interop. server2003</span><span class="sxs-lookup"><span data-stu-id="97001-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
