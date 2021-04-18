---
description: Дополнительные сведения о методе API. Жеткоммиттрансактион
title: API. Жеткоммиттрансактион, метод
TOCTitle: 'JetCommitTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.CommitTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcommittransaction(v=EXCHG.10)
ms:contentKeyID: 55100665
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edf0799af53c3da422f92f981f7a28ee7a283d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710852"
---
# <a name="apijetcommittransaction-method"></a>API. Жеткоммиттрансактион, метод

Фиксирует изменения, внесенные в состояние базы данных во время текущей точки сохранения, и переносит их в предыдущую точку сохранения. При фиксации самой внешней точки сохранения изменения, внесенные во время этой точки сохранения, будут зафиксированы в состоянии базы данных, и сеанс завершит транзакцию.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetCommitTransaction ( _
    sesid As JET_SESID, _
    grbit As CommitTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As CommitTransactionGrbitApi.JetCommitTransaction(sesid, _
    grbit)
```

``` csharp
public static void JetCommitTransaction(
    JET_SESID sesid,
    CommitTransactionGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Сеанс, для которого зафиксирована транзакция.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. коммиттрансактионгрбит](./committransactiongrbit-enumeration.md)  
    
    Параметры фиксации.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
