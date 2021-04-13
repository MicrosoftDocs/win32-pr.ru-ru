---
description: Дополнительные сведения о методе Transaction. Commit (Коммиттрансактионгрбит)
title: Метод Transaction. Commit (Коммиттрансактионгрбит)
TOCTitle: Commit method (CommitTransactionGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.Commit(Microsoft.Isam.Esent.Interop.CommitTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.commit(v=EXCHG.10)
ms:contentKeyID: 55104071
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.Commit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 048071a08d1211d6091fb6c2c23f9cfe302f8872
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265705"
---
# <a name="transactioncommit-method-committransactiongrbit"></a><span data-ttu-id="19909-103">Метод Transaction. Commit (Коммиттрансактионгрбит)</span><span class="sxs-lookup"><span data-stu-id="19909-103">Transaction.Commit method (CommitTransactionGrbit)</span></span>

<span data-ttu-id="19909-104">Фиксация транзакции.</span><span class="sxs-lookup"><span data-stu-id="19909-104">Commit a transaction.</span></span> <span data-ttu-id="19909-105">Этот объект должен находиться в транзакции.</span><span class="sxs-lookup"><span data-stu-id="19909-105">This object should be in a transaction.</span></span>

<span data-ttu-id="19909-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="19909-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="19909-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="19909-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="19909-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19909-108">Syntax</span></span>

``` vb
'Declaration
Public Sub Commit ( _
    grbit As CommitTransactionGrbit _
)
'Usage
Dim instance As Transaction
Dim grbit As CommitTransactionGrbit

instance.Commit(grbit)
```

``` csharp
public void Commit(
    CommitTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="19909-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="19909-109">Parameters</span></span>

  - <span data-ttu-id="19909-110">грбит</span><span class="sxs-lookup"><span data-stu-id="19909-110">grbit</span></span>  
    <span data-ttu-id="19909-111">Тип: [Microsoft. ISAM. ESENT. Interop. коммиттрансактионгрбит](./committransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="19909-111">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="19909-112">Параметры Жеткоммиттрансактион.</span><span class="sxs-lookup"><span data-stu-id="19909-112">JetCommitTransaction options.</span></span>

## <a name="see-also"></a><span data-ttu-id="19909-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19909-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="19909-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="19909-114">Reference</span></span>

[<span data-ttu-id="19909-115">класс Transaction</span><span class="sxs-lookup"><span data-stu-id="19909-115">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="19909-116">Элементы транзакции</span><span class="sxs-lookup"><span data-stu-id="19909-116">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="19909-117">Перегрузка фиксации</span><span class="sxs-lookup"><span data-stu-id="19909-117">Commit overload</span></span>](./transaction.commit-method.md)

[<span data-ttu-id="19909-118">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="19909-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
