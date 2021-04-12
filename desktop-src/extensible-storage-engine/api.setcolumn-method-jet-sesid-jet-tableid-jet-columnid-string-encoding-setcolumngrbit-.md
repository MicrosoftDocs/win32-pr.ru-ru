---
description: Дополнительные сведения см. в статье метод API. Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, строка, кодировка, Сетколумнгрбит).
title: Метод API. Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, строка, кодировка, Сетколумнгрбит)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding, SetColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.String,System.Text.Encoding,Microsoft.Isam.Esent.Interop.SetColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100886
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3f208f6d07bb7bf02c352263933f7eff68613d37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342585"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-string-encoding-setcolumngrbit"></a>Метод API. Сетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, строка, кодировка, Сетколумнгрбит)

Изменяет значение одного столбца в измененной записи для вставки или для обновления текущей записи.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As String, _
    encoding As Encoding, _
    grbit As SetColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As String
Dim encoding As Encoding
Dim grbit As SetColumnGrbitApi.SetColumn(sesid, tableid, columnid, _
    data, encoding, grbit)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    string data,
    Encoding encoding,
    SetColumnGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Обновляемый курсор. Необходимо подготовить обновление.

<!-- end list -->

  - columnid  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Устанавливаемое значение columnid.

<!-- end list -->

  - .  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Задаваемые данные.

<!-- end list -->

  - encoding  
    Тип: [System. Text. Encoding](/dotnet/api/system.text.encoding)  
    
    Кодировка, используемая для преобразования строки.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. сетколумнгрбит](./setcolumngrbit-enumeration.md)  
    
    Параметры Сетколумн.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Перегрузка Сетколумн](./api.setcolumn-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
