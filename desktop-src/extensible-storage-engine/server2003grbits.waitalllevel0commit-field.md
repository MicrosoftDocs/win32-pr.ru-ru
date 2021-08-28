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
ms.openlocfilehash: 3c6f3946d12b7614818545abc785d521e46b9c05ddedcffab09750846861782e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093174"
---
# <a name="server2003grbitswaitalllevel0commit-field"></a>Server2003Grbits. WaitAllLevel0Commit, поле

Все транзакции, ранее зафиксированные любым сеансом, которые еще не были сброшены в файл журнала транзакций, будут сброшены немедленно. Этот API будет ожидать, пока транзакции не будут сброшены перед возвратом в вызывающий объект. Этот параметр может использоваться, даже если сеанс в данный момент не находится в транзакции. Этот параметр нельзя использовать в сочетании с любым другим параметром.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

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

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Server2003Grbits](./server2003grbits-class.md)

[Элементы Server2003Grbits](./server2003grbits-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
