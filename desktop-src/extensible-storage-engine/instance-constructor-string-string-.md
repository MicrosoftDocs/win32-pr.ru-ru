---
description: 'Дополнительные сведения: конструктор экземпляров (строка, строка)'
title: Конструктор экземпляров (строка, строка)
TOCTitle: Instance constructor (String, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103267
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d93a5799a646a90688261bdd55bc9dfe929ef6bd074a51e15cabdcee768ffa2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116444"
---
# <a name="instance-constructor-string-string"></a>Конструктор экземпляров (строка, строка)

Инициализирует новый экземпляр класса экземпляра. Базовый JET_INSTANCE выделяется, но не инициализируется.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String _
)
'Usage
Dim name As String
Dim displayName As String

Dim instance As New Instance(name, displayName)
```

``` csharp
public Instance(
    string name,
    string displayName
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

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс экземпляра](./instance-class.md)

[Члены экземпляра](./instance-members.md)

[Перегрузка экземпляра](./instance-constructor.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
