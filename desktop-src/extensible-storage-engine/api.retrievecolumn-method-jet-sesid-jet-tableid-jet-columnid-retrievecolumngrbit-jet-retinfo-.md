---
description: 'Дополнительные сведения: метод API. Ретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит, JET_RETINFO)'
title: Метод API. Ретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит, JET_RETINFO)
TOCTitle: RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100853
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43657ec60e521795ba4d474306de9380618cd21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701341"
---
# <a name="apiretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit-jet_retinfo"></a>Метод API. Ретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит, JET_RETINFO)

Извлекает значение одного столбца из текущей записи. Запись — это запись, связанная с записью индекса в текущем положении курсора. Кроме того, эта функция может извлекать столбец из записи, создаваемой в буфере копирования курсора. Эта функция также может получать данные столбца из записи индекса, которая ссылается на текущую запись. Помимо получения фактического значения столбца, Жетретриевеколумн можно также использовать для получения размера столбца перед извлечением самих данных столбца, чтобы можно было соответствующим образом изменить размер буферов приложения.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Function RetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As Byte()

returnValue = Api.RetrieveColumn(sesid, _
    tableid, columnid, grbit, retinfo)
```

``` csharp
public static byte[] RetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Курсор, из которого извлекается столбец.

<!-- end list -->

  - columnid  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Значение columnid, которое необходимо получить.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. ретриевеколумнгрбит](./retrievecolumngrbit-enumeration.md)  
    
    Получение параметров столбца.

<!-- end list -->

  - ретинфо  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_RETINFO](./jet-retinfo-class.md)  
    
    Если претинфо имеет значение NULL, функция ведет себя так, как будто Итагсекуенце равен 1 и Иблонгвалуе 0 (нуль). Это приводит к извлечению столбца для получения первого значения многозначного столбца, а также для получения длинных данных со смещением 0 (нулем).

#### <a name="return-value"></a>Возвращаемое значение

Тип \[\]  
Данные, полученные из столбца. Значение null, если столбец имеет значение null.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Перегрузка Ретриевеколумн](./api.retrievecolumn-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
