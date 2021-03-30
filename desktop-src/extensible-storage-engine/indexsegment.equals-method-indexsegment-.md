---
description: 'Дополнительные сведения о методе: Индекссегмент. Equals (Индекссегмент)'
title: Метод Индекссегмент. Equals (Индекссегмент)
TOCTitle: Equals method (IndexSegment)
ms:assetid: M:Microsoft.Isam.Esent.Interop.IndexSegment.Equals(Microsoft.Isam.Esent.Interop.IndexSegment)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexsegment.equals(v=EXCHG.10)
ms:contentKeyID: 55103276
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.IndexSegment.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad14e8a22ab3e64f9df870f1e0a218e83f30a0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263385"
---
# <a name="indexsegmentequals-method-indexsegment"></a>Метод Индекссегмент. Equals (Индекссегмент)

Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Function Equals ( _
    other As IndexSegment _
) As Boolean
'Usage
Dim instance As IndexSegment
Dim other As IndexSegment
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    IndexSegment other
)
```

#### <a name="parameters"></a>Параметры

  - др.  
    Тип: [Microsoft. ISAM. ESENT. Interop. индекссегмент](./indexsegment-class.md)  
    
    Экземпляр, сравниваемый с этим экземпляром.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если два экземпляра равны.  

#### <a name="implements"></a>Реализации

[IEquatable \<T\> . Equals (T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Индекссегмент](./indexsegment-class.md)

[Элементы Индекссегмент](./indexsegment-members.md)

[Перегрузка Equals](./indexsegment.equals-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
