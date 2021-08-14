---
description: 'Дополнительные сведения: неявное преобразование сеанса (сеанс для JET_SESID)'
title: Неявное преобразование сеанса (сеанс для JET_SESID)
TOCTitle: Implicit conversion (Session to JET_SESID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.op_Implicit(Microsoft.Isam.Esent.Interop.Session)~Microsoft.Isam.Esent.Interop.JET_SESID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104121
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session.op_Implicit
- Microsoft.Isam.Esent.Interop.Session.Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be293636044e744ec02e3bdcddbc96b61373a35c9bddc04a03d282fcebe268d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118485513"
---
# <a name="session-implicit-conversion-session-to-jet_sesid"></a>Неявное преобразование сеанса (сеанс для JET_SESID)

Неявный оператор преобразования из сеанса в JET_SESID. Это позволяет использовать сеанс с интерфейсами API, которые предполагают JET_SESID.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    session As Session _
) As JET_SESID
'Usage
Dim input As Session
Dim output As JET_SESID

output = CType(input, JET_SESID)
```

``` csharp
public static implicit operator JET_SESID (
    Session session
)
```

#### <a name="parameters"></a>Параметры

  - сеанс  
    Тип: [Microsoft. ISAM. ESENT. Interop. Session](./session-class.md)  
    
    Преобразуемый сеанс.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
JET_SESID сеанса.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Session class](./session-class.md)

[Члены сеанса](./session-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
