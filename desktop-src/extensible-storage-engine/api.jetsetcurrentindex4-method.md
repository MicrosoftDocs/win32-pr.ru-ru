---
description: Дополнительные сведения о методе API. JetSetCurrentIndex4
title: API. JetSetCurrentIndex4, метод
TOCTitle: 'JetSetCurrentIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex4(v=EXCHG.10)
ms:contentKeyID: 55100806
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2b9319554b998175b3f533c6cd5f4c2d05ba02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673217"
---
# <a name="apijetsetcurrentindex4-method"></a>API. JetSetCurrentIndex4, метод

Задает текущий индекс курсора.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    indexid As JET_INDEXID, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim indexid As JET_INDEXID
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex4(sesid, _
    tableid, index, indexid, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    JET_INDEXID indexid,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Курсор, для которого задается индекс.

<!-- end list -->

  - index  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Имя выбранного индекса. Если это значение равно null или пуст, первичный индекс будет выбран.

<!-- end list -->

  - indexid  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)  
    
    Идентификатор выбираемого индекса. Этот идентификатор можно получить с помощью Жетжетиндексинфо или Жетжеттаблеиндексинфо с параметром [индексид](./jet-idxinfo-enumeration.md) .

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. сеткуррентиндексгрбит](./setcurrentindexgrbit-enumeration.md)  
    
    Задайте параметры индекса.

<!-- end list -->

  - итагсекуенце  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Порядковый номер значения столбца с несколькими значениями, который будет использоваться для позиционирования курсора на новом индексе. Этот параметр используется только в сочетании с параметром [OnMove](./setcurrentindexgrbit-enumeration.md). Если этот параметр отсутствует или имеет значение 0, предполагается, что оно равно 1.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
