---
description: 'Дополнительные сведения о: JET_THREADSTATS. Создать метод'
title: JET_THREADSTATS. Метод Create (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Create method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create(System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.create(v=EXCHG.10)
ms:contentKeyID: 39509886
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: beaaee85fc0f6c331db1d813280d4b900e39fb54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816345"
---
# <a name="jet_threadstatscreate-method"></a>JET_THREADSTATS. Создать метод

Создать новую [JET_THREADSTATS](./jet-threadstats-structure2.md) структуру с указанным значением.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Function Create ( _
    cPageReferenced As Integer, _
    cPageRead As Integer, _
    cPagePreread As Integer, _
    cPageDirtied As Integer, _
    cPageRedirtied As Integer, _
    cLogRecord As Integer, _
    cbLogRecord As Integer _
) As JET_THREADSTATS
'Usage
Dim cPageReferenced As Integer
Dim cPageRead As Integer
Dim cPagePreread As Integer
Dim cPageDirtied As Integer
Dim cPageRedirtied As Integer
Dim cLogRecord As Integer
Dim cbLogRecord As Integer
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Create(cPageReferenced, _
    cPageRead, cPagePreread, cPageDirtied, _
    cPageRedirtied, cLogRecord, cbLogRecord)
```

``` csharp
public static JET_THREADSTATS Create(
    int cPageReferenced,
    int cPageRead,
    int cPagePreread,
    int cPageDirtied,
    int cPageRedirtied,
    int cLogRecord,
    int cbLogRecord
)
```

#### <a name="parameters"></a>Параметры

  - кпажереференцед  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Количество посещенных страниц.

<!-- end list -->

  - кпажереад  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Число прочитанных страниц.

<!-- end list -->

  - кпажепререад  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Число страниц, которые были считаны.

<!-- end list -->

  - кпажедиртиед  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Тнумбер страниц изменялся.

<!-- end list -->

  - кпажередиртиед  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Число страниц редиртиед.

<!-- end list -->

  - клогрекорд  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Число созданных записей журнала.

<!-- end list -->

  - кблогрекорд  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Байтов записанных записей журнала.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
Новая [JET_THREADSTATS](./jet-threadstats-structure2.md) структура с указанными значениями.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_THREADSTATS](./jet-threadstats-structure2.md)

[Элементы JET_THREADSTATS](./jet-threadstats-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
