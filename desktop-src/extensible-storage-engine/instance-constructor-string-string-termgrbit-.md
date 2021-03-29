---
description: 'Дополнительные сведения: конструктор экземпляров (строка, строка, Термгрбит)'
title: Конструктор экземпляров (строка, строка, Термгрбит)
TOCTitle: Instance constructor (String, String, TermGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103289
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9cf90f9678db1074594c7772eb67d895a8a5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811128"
---
# <a name="instance-constructor-string-string-termgrbit"></a>Конструктор экземпляров (строка, строка, Термгрбит)

Инициализирует новый экземпляр класса экземпляра. Базовый JET_INSTANCE выделяется, но не инициализируется.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String, _
    termGrbit As TermGrbit _
)
'Usage
Dim name As String
Dim displayName As String
Dim termGrbit As TermGrbit

Dim instance As New Instance(name, displayName, _
    termGrbit)
```

``` csharp
public Instance(
    string name,
    string displayName,
    TermGrbit termGrbit
)
```

#### <a name="parameters"></a>Параметры

  - name  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Имя экземпляра. Эта строка должна быть уникальной в пределах данного процесса, в котором размещается ядро СУБД.

<!-- end list -->

  - displayName  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Отображаемое имя экземпляра. Он будет использоваться в записях журнала событий.

<!-- end list -->

  - термгрбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. термгрбит](./termgrbit-enumeration.md)  
    
    Термгрбит, который будет использоваться во время Жеттерм.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс экземпляра](./instance-class.md)

[Члены экземпляра](./instance-members.md)

[Перегрузка экземпляра](./instance-constructor.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
