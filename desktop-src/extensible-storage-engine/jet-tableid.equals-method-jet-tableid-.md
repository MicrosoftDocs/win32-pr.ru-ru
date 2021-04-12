---
description: 'Дополнительные сведения о: JET_TABLEID. Метод Equals (JET_TABLEID)'
title: JET_TABLEID. Метод Equals (JET_TABLEID)
TOCTitle: Equals method (JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.Equals(Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.equals(v=EXCHG.10)
ms:contentKeyID: 39514708
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2eab8bae322c7b19b5aada08801f752ad6bfaa93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265724"
---
# <a name="jet_tableidequals-method-jet_tableid"></a>JET_TABLEID. Метод Equals (JET_TABLEID)

Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Function Equals ( _
    other As JET_TABLEID _
) As Boolean
'Usage
Dim instance As JET_TABLEID
Dim other As JET_TABLEID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_TABLEID other
)
```

#### <a name="parameters"></a>Параметры

  - др.  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Экземпляр, сравниваемый с этим экземпляром.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если два экземпляра равны.  

#### <a name="implements"></a>Реализации

[IEquatable \<T\> . Equals (T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_TABLEID](./jet-tableid-structure.md)

[Элементы JET_TABLEID](./jet-tableid-members.md)

[Перегрузка Equals](./jet-tableid.equals-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
