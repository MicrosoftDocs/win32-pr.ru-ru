---
description: 'Дополнительные сведения о свойстве: SystemParameters. Енаблевиевкаче'
title: SystemParameters. Енаблевиевкаче, свойство
TOCTitle: 'EnableViewCache property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableViewCache
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enableviewcache(v=EXCHG.10)
ms:contentKeyID: 55104120
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableViewCache
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableViewCache
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableViewCache
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableViewCache
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b22808109b8fd69df18b9a6ae98de17a814b5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272984"
---
# <a name="systemparametersenableviewcache-property"></a>SystemParameters. Енаблевиевкаче, свойство

Возвращает или задает значение, указывающее, следует ли ядру СУБД использовать файловый ввод-вывод, размещенный в памяти, для файлов базы данных.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Property EnableViewCache As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableViewCache

SystemParameters.EnableViewCache = value
```

``` csharp
public static bool EnableViewCache { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[SystemParameters - класс](./systemparameters-class.md)

[Элементы SystemParameters](./systemparameters-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
