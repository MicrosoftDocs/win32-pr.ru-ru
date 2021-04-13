---
description: Дополнительные сведения о методе API. Жеткомпутестатс
title: API. Жеткомпутестатс, метод
TOCTitle: 'JetComputeStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetComputeStats(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcomputestats(v=EXCHG.10)
ms:contentKeyID: 55100667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b102aca5971656232fae02684aeab30322d208b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262839"
---
# <a name="apijetcomputestats-method"></a>API. Жеткомпутестатс, метод

Просматривает каждый индекс таблицы, чтобы точно вычислить количество записей в индексе и количество различных ключей в индексе. Эти сведения вместе с количеством страниц базы данных, выделенных для индекса, и текущим временем вычислений хранятся в метаданных индекса в базе данных. Эти данные можно впоследствии извлечь с помощью информационных операций.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetComputeStats ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetComputeStats(sesid, tableid)
```

``` csharp
public static void JetComputeStats(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Таблица, для которой будет вычисляться статистика.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
