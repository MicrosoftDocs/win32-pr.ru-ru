---
description: Дополнительные сведения о методе API. Жетретриевекэй
title: API. Жетретриевекэй, метод
TOCTitle: 'JetRetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievekey(v=EXCHG.10)
ms:contentKeyID: 55100795
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 161840971181db3594257b1ae2440c3c1c06b35a871b21c4cbeddad56527a9d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118783905"
---
# <a name="apijetretrievekey-method"></a>API. Жетретриевекэй, метод

Возвращает ключ для записи индекса в текущем положении курсора. См. также [ретриевекэй (JET_SESID, JET_TABLEID, ретриевекэйгрбит)](./api.retrievekey-method.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetRetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveKeyGrbitApi.JetRetrieveKey(sesid, tableid, _
    data, dataSize, actualDataSize, grbit)
```

``` csharp
public static void JetRetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Курсор, из которого извлекается ключ.

<!-- end list -->

  - .  
    Тип \[\]  
    
    Буфер, в который извлекается ключ.

<!-- end list -->

  - dataSize  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Размер буфера.

<!-- end list -->

  - актуалдатасизе  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Возвращает фактический размер данных.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. ретриевекэйгрбит](./retrievekeygrbit-enumeration.md)  
    
    Получение параметров ключа.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
