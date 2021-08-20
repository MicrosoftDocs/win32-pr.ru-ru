---
description: 'Дополнительные сведения о: JET_DBINFOMISC. Метод Equals (JET_DBINFOMISC)'
title: JET_DBINFOMISC. Метод Equals (JET_DBINFOMISC)
TOCTitle: Equals method (JET_DBINFOMISC)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals(Microsoft.Isam.Esent.Interop.JET_DBINFOMISC)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.equals(v=EXCHG.10)
ms:contentKeyID: 39514332
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b16ec19a26ca02953de3028d91a54ecd440e7831472bbaa0baba6b8a40e5d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117895059"
---
# <a name="jet_dbinfomiscequals-method-jet_dbinfomisc"></a>JET_DBINFOMISC. Метод Equals (JET_DBINFOMISC)

Указывает, равен ли текущий объект другому объекту того же типа.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Function Equals ( _
    other As JET_DBINFOMISC _
) As Boolean
'Usage
Dim instance As JET_DBINFOMISC
Dim other As JET_DBINFOMISC
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_DBINFOMISC other
)
```

#### <a name="parameters"></a>Параметры

  - др.  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)  
    
    Объект, который требуется сравнить с данным объектом.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если текущий объект равен другому параметру; в противном случае — значение false.  

#### <a name="implements"></a>Реализации

[IEquatable \<T\> . Equals (T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс JET_DBINFOMISC](./jet-dbinfomisc-class.md)

[Элементы JET_DBINFOMISC](./jet-dbinfomisc-members.md)

[Перегрузка Equals](./jet-dbinfomisc.equals-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
