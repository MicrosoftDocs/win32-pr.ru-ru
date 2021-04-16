---
description: 'Дополнительные сведения о: конструктор Есентресаурцеексцептион (String, JET_err)'
title: Конструктор Есентресаурцеексцептион (String, JET_err)
TOCTitle: EsentResourceException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResourceException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55107307
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 458b12a80fdc0e6d7883d966f2e50aa8c1f6d69b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545970"
---
# <a name="esentresourceexception-constructor-string-jet_err"></a>Конструктор Есентресаурцеексцептион (String, JET_err)

Инициализирует новый экземпляр класса Есентресаурцеексцептион.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentResourceException(description, _
    err)
```

``` csharp
protected EsentResourceException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a>Параметры

  - description;  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Описание ошибки.

<!-- end list -->

  - Err  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)  
    
    Код ошибки исключения.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс EsentResourceException](./esentresourceexception-class.md)

[Элементы Есентресаурцеексцептион](./esentresourceexception-members.md)

[Перегрузка Есентресаурцеексцептион](./esentresourceexception-constructor.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
