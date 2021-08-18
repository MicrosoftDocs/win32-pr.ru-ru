---
description: 'Дополнительные сведения о: конструктор Есенткорруптионексцептион (String, JET_err)'
title: Конструктор Есенткорруптионексцептион (String, JET_err)
TOCTitle: EsentCorruptionException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentCorruptionException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101380
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbf059d91d1782588b8f9211b888d7b12b752abbff2637ae1f3f492eb312c6f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736597"
---
# <a name="esentcorruptionexception-constructor-string-jet_err"></a>Конструктор Есенткорруптионексцептион (String, JET_err)

Инициализирует новый экземпляр класса Есенткорруптионексцептион.

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

Dim instance As New EsentCorruptionException(description, _
    err)
```

``` csharp
protected EsentCorruptionException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a>Параметры

  - description  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Описание ошибки.

<!-- end list -->

  - Err  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)  
    
    Код ошибки исключения.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс EsentCorruptionException](./esentcorruptionexception-class.md)

[Элементы Есенткорруптионексцептион](./esentcorruptionexception-members.md)

[Перегрузка Есенткорруптионексцептион](./esentcorruptionexception-constructor.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
