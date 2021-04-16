---
description: Дополнительные сведения о методе API. Жетендсессион
title: API. Жетендсессион, метод
TOCTitle: 'JetEndSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndSession(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.EndSessionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendsession(v=EXCHG.10)
ms:contentKeyID: 55100690
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndSession
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10412f6b01b14d63557bf024d65975c271bbe31b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540858"
---
# <a name="apijetendsession-method"></a>API. Жетендсессион, метод

Завершает сеанс.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetEndSession ( _
    sesid As JET_SESID, _
    grbit As EndSessionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As EndSessionGrbitApi.JetEndSession(sesid, grbit)
```

``` csharp
public static void JetEndSession(
    JET_SESID sesid,
    EndSessionGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Сеанс, который необходимо завершить.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. ендсессионгрбит](./endsessiongrbit-enumeration.md)  
    
    Этот параметр не используется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
