---
description: Дополнительные сведения о методе API. Жетсик
title: API. Жетсик, метод
TOCTitle: 'JetSeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetseek(v=EXCHG.10)
ms:contentKeyID: 55100796
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85c8c61bd4e56b342b33d26f22ae3946967640e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999551"
---
# <a name="apijetseek-method"></a>API. Жетсик, метод

Эффективно позиционирует курсор на запись индекса, которая соответствует условиям поиска, заданным в ключе поиска в этом курсоре, и заданному неравенству. Ключ поиска должен быть ранее создан с помощью [жетмакекэй (JET_SESID, JET_TABLEID, \[ \] , Int32, макекэйгрбит)](./api.jetmakekey-method.md). См. также [трисик (JET_SESID, JET_TABLEID, сикгрбит)](./api.tryseek-method.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Function JetSeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetSeek(sesid, _
    tableid, grbit)
```

``` csharp
public static JET_wrn JetSeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Курсор для позиции.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. сикгрбит](./seekgrbit-enumeration.md)  
    
    Параметры поиска.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Предупреждение ESENT.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
