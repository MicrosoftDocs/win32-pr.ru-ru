---
description: 'Дополнительные сведения о: JET_SIGNATURE. Метод Equals (JET_SIGNATURE)'
title: JET_SIGNATURE. Метод Equals (JET_SIGNATURE)
TOCTitle: Equals method (JET_SIGNATURE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equals(Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.equals(v=EXCHG.10)
ms:contentKeyID: 39511830
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5f099b74af84e1a75289313c5bb9d4de646b51a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542583"
---
# <a name="jet_signatureequals-method-jet_signature"></a>JET_SIGNATURE. Метод Equals (JET_SIGNATURE)

Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Function Equals ( _
    other As JET_SIGNATURE _
) As Boolean
'Usage
Dim instance As JET_SIGNATURE
Dim other As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_SIGNATURE other
)
```

#### <a name="parameters"></a>Параметры

  - др.  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)  
    
    Экземпляр, сравниваемый с этим экземпляром.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если два экземпляра равны.  

#### <a name="implements"></a>Реализации

[IEquatable \<T\> . Equals (T)](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_SIGNATURE](./jet-signature-structure2.md)

[Элементы JET_SIGNATURE](./jet-signature-members.md)

[Перегрузка Equals](./jet-signature.equals-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
