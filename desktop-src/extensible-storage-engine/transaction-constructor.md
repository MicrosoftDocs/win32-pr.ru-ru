---
description: 'Дополнительные сведения: конструктор транзакций'
title: Конструктор транзакций
TOCTitle: 'Transaction constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.transaction(v=EXCHG.10)
ms:contentKeyID: 55104069
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Transaction.Transaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Transaction..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a8c3214ebe3d88ce8b50aff000d64270ec50a6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265711"
---
# <a name="transaction-constructor"></a><span data-ttu-id="56dca-103">Конструктор транзакций</span><span class="sxs-lookup"><span data-stu-id="56dca-103">Transaction constructor</span></span>

<span data-ttu-id="56dca-104">Инициализирует новый экземпляр класса Transaction.</span><span class="sxs-lookup"><span data-stu-id="56dca-104">Initializes a new instance of the Transaction class.</span></span> <span data-ttu-id="56dca-105">Это автоматически начнет транзакцию.</span><span class="sxs-lookup"><span data-stu-id="56dca-105">This automatically begins a transaction.</span></span> <span data-ttu-id="56dca-106">Если не зафиксировано явно, будет выполнен откат транзакции.</span><span class="sxs-lookup"><span data-stu-id="56dca-106">The transaction will be rolled back if not explicitly committed.</span></span>

<span data-ttu-id="56dca-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="56dca-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="56dca-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="56dca-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="56dca-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56dca-109">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESID

Dim instance As New Transaction(sesid)
```

``` csharp
public Transaction(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="56dca-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="56dca-110">Parameters</span></span>

  - <span data-ttu-id="56dca-111">сесид</span><span class="sxs-lookup"><span data-stu-id="56dca-111">sesid</span></span>  
    <span data-ttu-id="56dca-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="56dca-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="56dca-113">Сеанс, для которого запускается транзакция.</span><span class="sxs-lookup"><span data-stu-id="56dca-113">The session to start the transaction for.</span></span>

## <a name="see-also"></a><span data-ttu-id="56dca-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56dca-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="56dca-115">Справочник</span><span class="sxs-lookup"><span data-stu-id="56dca-115">Reference</span></span>

[<span data-ttu-id="56dca-116">класс Transaction</span><span class="sxs-lookup"><span data-stu-id="56dca-116">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="56dca-117">Элементы транзакции</span><span class="sxs-lookup"><span data-stu-id="56dca-117">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="56dca-118">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="56dca-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
