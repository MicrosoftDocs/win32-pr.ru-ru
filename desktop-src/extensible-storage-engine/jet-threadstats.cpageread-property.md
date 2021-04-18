---
description: 'Дополнительные сведения о свойстве: JET_THREADSTATS. Кпажереад'
title: Свойство JET_THREADSTATS. Кпажереад (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cPageRead property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRead
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpageread(v=EXCHG.10)
ms:contentKeyID: 39516296
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRead
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPageRead
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRead
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPageRead
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4c5a8ed28a4f45abe57ca71eff89ab2ce374bf0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712729"
---
# <a name="jet_threadstatscpageread-property"></a>Свойство JET_THREADSTATS. Кпажереад

Возвращает общее число страниц базы данных, извлекаемых с диска ядром СУБД в текущем потоке.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property cPageRead As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPageRead
```

``` csharp
public int cPageRead { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_THREADSTATS](./jet-threadstats-structure2.md)

[Элементы JET_THREADSTATS](./jet-threadstats-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
