---
description: 'Дополнительные сведения о методе: Windows8Api. JetCreateIndex4'
title: Windows8Api. JetCreateIndex4, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetCreateIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_INDEXCREATE[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcreateindex4(v=EXCHG.10)
ms:contentKeyID: 55104455
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc06fa47b8463c6c3b731a7e0e06b7ba13ae687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155219"
---
# <a name="windows8apijetcreateindex4-method"></a>Windows8Api. JetCreateIndex4, метод

Создает индексы для данных в базе данных ESE.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetCreateIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexcreates As JET_INDEXCREATE(), _
    numIndexCreates As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexcreates As JET_INDEXCREATE()
Dim numIndexCreates As IntegerWindows8Api.JetCreateIndex4(sesid, tableid, _
    indexcreates, numIndexCreates)
```

``` csharp
public static void JetCreateIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEXCREATE[] indexcreates,
    int numIndexCreates
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Таблица, в которой создается индекс.

<!-- end list -->

  - индекскреатес  
    Тип \[\]  
    
    Массив объектов, описывающих создаваемые индексы.

<!-- end list -->

  - нуминдекскреатес  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Число объектов описания индекса.

## <a name="remarks"></a>Комментарии

При создании нескольких индексов (т. е. с Нуминдекскреатес больше 1) Этот метод должен вызываться за пределами транзакций и с монопольным доступом к таблице. JET_TABLEID, возвращаемый "API. Жеткреатетабле", будет иметь доступ только, или таблицу можно открыть для монопольного доступа, передав [дениреад](./opentablegrbit-enumeration.md) в [жетопентабле (JET_SESID, JET_DBID, String, \[ \] , Int32, опентаблегрбит, JET_TABLEID)](./api.jetopentable-method.md).

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Windows8Api](./windows8api-class.md)

[Элементы Windows8Api](./windows8api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
