---
description: 'Дополнительные сведения о свойстве: JET_THREADSTATS. Кпажередиртиед'
title: Свойство JET_THREADSTATS. Кпажередиртиед (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cPageRedirtied property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRedirtied
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpageredirtied(v=EXCHG.10)
ms:contentKeyID: 39515312
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRedirtied
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRedirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPageRedirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPageRedirtied
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23f17641957ebc51216768e45cd2c4dac6565dc5b43eec3b782719fe9bb49d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118073069"
---
# <a name="jet_threadstatscpageredirtied-property"></a>Свойство JET_THREADSTATS. Кпажередиртиед

Возвращает общее число страниц базы данных с незаписанными изменениями, которые были изменены ядром СУБД в текущем потоке.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property cPageRedirtied As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPageRedirtied
```

``` csharp
public int cPageRedirtied { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Структура JET_THREADSTATS](./jet-threadstats-structure2.md)

[Элементы JET_THREADSTATS](./jet-threadstats-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
