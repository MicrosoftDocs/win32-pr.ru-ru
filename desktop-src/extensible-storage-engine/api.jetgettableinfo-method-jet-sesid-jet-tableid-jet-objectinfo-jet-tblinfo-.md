---
description: 'Дополнительные сведения: метод API. Жетжеттаблеинфо (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)'
title: Метод API. Жетжеттаблеинфо (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_OBJECTINFO@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100739
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fbc95c771e2610ec23bdf503cdefa0399ee219ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711337"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-jet_objectinfo-jet_tblinfo"></a>Метод API. Жетжеттаблеинфо (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)

Извлекает различные фрагменты информации о таблице в базе данных.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As JET_OBJECTINFO, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As JET_OBJECTINFO
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_OBJECTINFO result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Таблица, сведения о которой необходимо получить.

<!-- end list -->

  - result  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)  
    
    Извлеченные сведения.

<!-- end list -->

  - инфолевел  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)  
    
    Тип извлекаемых данных.

## <a name="remarks"></a>Комментарии

Эта перегрузка используется со [значением по умолчанию](./jet-tblinfo-enumeration.md).

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Перегрузка Жетжеттаблеинфо](./api.jetgettableinfo-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
