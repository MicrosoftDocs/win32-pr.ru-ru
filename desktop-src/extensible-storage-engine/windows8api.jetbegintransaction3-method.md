---
description: 'Дополнительные сведения о методе: Windows8Api. JetBeginTransaction3'
title: Windows8Api. JetBeginTransaction3, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetBeginTransaction3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3(Microsoft.Isam.Esent.Interop.JET_SESID,System.Int64,Microsoft.Isam.Esent.Interop.BeginTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetbegintransaction3(v=EXCHG.10)
ms:contentKeyID: 55107825
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7605cdb44c66d929e6663caaad9e40d3c98737b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543650"
---
# <a name="windows8apijetbegintransaction3-method"></a>Windows8Api. JetBeginTransaction3, метод

Заставляет сеанс войти в транзакцию или создать новую точку сохранения в существующей транзакции.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetBeginTransaction3 ( _
    sesid As JET_SESID, _
    userTransactionId As Long, _
    grbit As BeginTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim userTransactionId As Long
Dim grbit As BeginTransactionGrbitWindows8Api.JetBeginTransaction3(sesid, _
    userTransactionId, grbit)
```

``` csharp
public static void JetBeginTransaction3(
    JET_SESID sesid,
    long userTransactionId,
    BeginTransactionGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Сеанс, для которого начинается транзакция.

<!-- end list -->

  - усертрансактионид  
    Тип: [System. Int64](/dotnet/api/system.int64)  
    
    Необязательный идентификатор, предоставленный пользователем для идентификации транзакции.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. бегинтрансактионгрбит](./begintransactiongrbit-enumeration.md)  
    
    Параметры транзакций.

## <a name="remarks"></a>Комментарии

Впервые появился в Windows 8.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Windows8Api](./windows8api-class.md)

[Элементы Windows8Api](./windows8api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
