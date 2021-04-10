---
description: 'Дополнительные сведения о: Есентинвалиддатабасеверсионексцептион Class'
title: Класс Есентинвалиддатабасеверсионексцептион
TOCTitle: EsentInvalidDatabaseVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvaliddatabaseversionexception(v=EXCHG.10)
ms:contentKeyID: 55101922
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24b3e348c0c0adaf4d261705c1e4de7bf5d7297b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273047"
---
# <a name="esentinvaliddatabaseversionexception-class"></a>Класс Есентинвалиддатабасеверсионексцептион

Базовый класс для JET_err. Исключения Инвалиддатабасеверсион.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион](./esentdataexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион](./esentinconsistentexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. Есентинвалиддатабасеверсионексцептион  

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidDatabaseVersionException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentInvalidDatabaseVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidDatabaseVersionException : EsentInconsistentException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы Есентинвалиддатабасеверсионексцептион](./esentinvaliddatabaseversionexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
