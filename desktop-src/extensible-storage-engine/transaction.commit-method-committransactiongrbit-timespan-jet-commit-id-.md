---
description: Дополнительные сведения о методе Transaction. Commit (Коммиттрансактионгрбит, TimeSpan, JET_COMMIT_ID)
title: Метод Transaction. Commit (Коммиттрансактионгрбит, TimeSpan, JET_COMMIT_ID)
TOCTitle: Commit method (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.Commit(Microsoft.Isam.Esent.Interop.CommitTransactionGrbit,System.TimeSpan,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.commit(v=EXCHG.10)
ms:contentKeyID: 55104166
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.Commit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18df363e4320a4b1a53c34e15fcf68939fce96ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081255"
---
# <a name="transactioncommit-method-committransactiongrbit-timespan-jet_commit_id"></a>Метод Transaction. Commit (Коммиттрансактионгрбит, TimeSpan, JET_COMMIT_ID)

Фиксация транзакции. Этот объект должен находиться в транзакции.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Sub Commit ( _
    grbit As CommitTransactionGrbit, _
    durableCommit As TimeSpan, _
    <OutAttribute> ByRef commitId As JET_COMMIT_ID _
)
'Usage
Dim instance As Transaction
Dim grbit As CommitTransactionGrbit
Dim durableCommit As TimeSpan
Dim commitId As JET_COMMIT_ID

instance.Commit(grbit, durableCommit, _
    commitId)
```

``` csharp
public void Commit(
    CommitTransactionGrbit grbit,
    TimeSpan durableCommit,
    out JET_COMMIT_ID commitId
)
```

#### <a name="parameters"></a>Параметры

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. коммиттрансактионгрбит](./committransactiongrbit-enumeration.md)  
    
    Параметры Жеткоммиттрансактион.

<!-- end list -->

  - дураблекоммит  
    Тип: [System. TimeSpan](/dotnet/api/system.timespan)  
    
    Длительность фиксации отложенных транзакций.

<!-- end list -->

  - коммитид  
    Тип: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Commit-ID для этой записи фиксации.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[класс Transaction](./transaction-class.md)

[Элементы транзакции](./transaction-members.md)

[Перегрузка фиксации](./transaction.commit-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
