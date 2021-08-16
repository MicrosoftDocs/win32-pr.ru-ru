---
description: 'Дополнительные сведения о: Server2003Param. Алтернатедатабасерековерипас поле'
title: Поле Server2003Param. Алтернатедатабасерековерипас (Microsoft. ISAM. ESENT. Interop. server2003)
TOCTitle: AlternateDatabaseRecoveryPath field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003param.alternatedatabaserecoverypath(v=EXCHG.10)
ms:contentKeyID: 55104217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a85673979a3b65d8c78ca06fae4496c11f8d2b31c810d411142e6c40bfd62cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107248"
---
# <a name="server2003paramalternatedatabaserecoverypath-field"></a>Server2003Param. Алтернатедатабасерековерипас, поле

Полный путь к каждой базе данных сохраняется в журналах транзакций во время выполнения. Обычно эти базы данных должны оставаться в исходном расположении для правильной работы воспроизведения транзакций. Этот параметр можно использовать для принудительного восстановления после сбоя или операции восстановления, чтобы найти базы данных, упоминаемые в журнале транзакций в указанной папке.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Const AlternateDatabaseRecoveryPath As JET_param
'Usage
Dim value As JET_param

value = Server2003Param.AlternateDatabaseRecoveryPath
```

``` csharp
public const JET_param AlternateDatabaseRecoveryPath
```

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Server2003Param](./server2003param-class.md)

[Элементы Server2003Param](./server2003param-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
