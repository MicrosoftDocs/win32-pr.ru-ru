---
description: Дополнительные сведения о методе API. Жетескровупдате
title: API. Жетескровупдате, метод
TOCTitle: 'JetEscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetescrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100740
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec5ddbedb921b89ef1b3c6e5bc48284da72407e8374bd6f0bb2de51c39c087e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042672"
---
# <a name="apijetescrowupdate-method"></a>API. Жетескровупдате, метод

Выполняет атомарную операцию сложения для одного столбца. Эта функция позволяет нескольким сеансам одновременно обновлять одну и ту же запись без конфликтов. См. также [ескровупдате (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetEscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Byte(), _
    deltaSize As Integer, _
    previousValue As Byte(), _
    previousValueLength As Integer, _
    <OutAttribute> ByRef actualPreviousValueLength As Integer, _
    grbit As EscrowUpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Byte()
Dim deltaSize As Integer
Dim previousValue As Byte()
Dim previousValueLength As Integer
Dim actualPreviousValueLength As Integer
Dim grbit As EscrowUpdateGrbitApi.JetEscrowUpdate(sesid, tableid, _
    columnid, delta, deltaSize, previousValue, _
    previousValueLength, actualPreviousValueLength, _
    grbit)
```

``` csharp
public static void JetEscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] delta,
    int deltaSize,
    byte[] previousValue,
    int previousValueLength,
    out int actualPreviousValueLength,
    EscrowUpdateGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс. Сеанс должен быть в транзакции.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Обновляемый курсор.

<!-- end list -->

  - columnid  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Обновляемый столбец. Это должен быть условно обновляемый столбец.

<!-- end list -->

  - delta  
    Тип \[\]  
    
    Буфер, содержащий слагаемое.

<!-- end list -->

  - делтасизе  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Размер слагаемое.

<!-- end list -->

  - превиаусвалуе  
    Тип \[\]  
    
    Выходной буфер, который получит текущее значение столбца. Этот буфер может иметь значение null.

<!-- end list -->

  - превиаусвалуеленгс  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Размер буфера Превиаусвалуе.

<!-- end list -->

  - актуалпревиаусвалуеленгс  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Возвращает фактический размер Превиаусвалуе.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. ескровупдатегрбит](./escrowupdategrbit-enumeration.md)  
    
    Параметры депонирования обновлений.

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
