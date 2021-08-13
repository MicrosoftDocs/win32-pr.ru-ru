---
description: Дополнительные сведения о методе API. JetDetachDatabase2
title: API. JetDetachDatabase2, метод
TOCTitle: 'JetDetachDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdetachdatabase2(v=EXCHG.10)
ms:contentKeyID: 55100685
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f90ed476fa691ffbc84496d6add48b2d502444af1777a952343c3162f6a5d7fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784346"
---
# <a name="apijetdetachdatabase2-method"></a>API. JetDetachDatabase2, метод

Освобождает файл базы данных, который был ранее присоединен к сеансу базы данных.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetDetachDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    grbit As DetachDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim grbit As DetachDatabaseGrbitApi.JetDetachDatabase2(sesid, database, _
    grbit)
```

``` csharp
public static void JetDetachDatabase2(
    JET_SESID sesid,
    string database,
    DetachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс базы данных.

<!-- end list -->

  - База данных  
    Тип: [System. String](/dotnet/api/system.string)  
    
    База данных для отсоединения.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. детачдатабасегрбит](./detachdatabasegrbit-enumeration.md)  
    
    Параметры отсоединения.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
