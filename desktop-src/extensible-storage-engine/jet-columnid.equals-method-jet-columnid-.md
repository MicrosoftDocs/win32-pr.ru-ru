---
description: 'Дополнительные сведения о: JET_COLUMNID. Метод Equals (JET_COLUMNID)'
title: JET_COLUMNID. Метод Equals (JET_COLUMNID)
TOCTitle: Equals method (JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.Equals(Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.equals(v=EXCHG.10)
ms:contentKeyID: 39516458
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb0cc59a465f48474e2fe63f5ef78f1fea85f37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263379"
---
# <a name="jet_columnidequals-method-jet_columnid"></a>JET_COLUMNID. Метод Equals (JET_COLUMNID)

Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Function Equals ( _
    other As JET_COLUMNID _
) As Boolean
'Usage
Dim instance As JET_COLUMNID
Dim other As JET_COLUMNID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_COLUMNID other
)
```

#### <a name="parameters"></a>Параметры

  - др.  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Экземпляр, сравниваемый с этим экземпляром.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если два экземпляра равны.  

#### <a name="implements"></a>Реализации

[IEquatable \<T\> . Equals (T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_COLUMNID](./jet-columnid-structure.md)

[Элементы JET_COLUMNID](./jet-columnid-members.md)

[Перегрузка Equals](./jet-columnid.equals-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
