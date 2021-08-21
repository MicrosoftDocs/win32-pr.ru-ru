---
description: 'Дополнительные сведения о свойстве: SystemParameters. Енаблефилекаче'
title: SystemParameters. Енаблефилекаче, свойство
TOCTitle: 'EnableFileCache property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableFileCache
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enablefilecache(v=EXCHG.10)
ms:contentKeyID: 55104039
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableFileCache
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableFileCache
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableFileCache
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableFileCache
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7c6635f4c7c4e6f82aa9c001fd60c7a4bbdc30b0b9b5878d320c77a1f2f1531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118484990"
---
# <a name="systemparametersenablefilecache-property"></a>SystemParameters. Енаблефилекаче, свойство

Возвращает или задает значение, указывающее, следует ли ядру СУБД использовать кэш файлов ОС для всех управляемых файлов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Property EnableFileCache As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableFileCache

SystemParameters.EnableFileCache = value
```

``` csharp
public static bool EnableFileCache { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[SystemParameters - класс](./systemparameters-class.md)

[Элементы SystemParameters](./systemparameters-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
