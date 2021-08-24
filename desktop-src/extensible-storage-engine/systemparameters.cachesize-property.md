---
description: 'Дополнительные сведения о свойстве: SystemParameters. CacheSize'
title: SystemParameters. CacheSize, свойство
TOCTitle: 'CacheSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.cachesize(v=EXCHG.10)
ms:contentKeyID: 55104109
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSize
- Microsoft.Isam.Esent.Interop.SystemParameters.set_CacheSize
- Microsoft.Isam.Esent.Interop.SystemParameters.get_CacheSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d3f059a40c5ec7bb35b90ec4cddf584d586ace3a039e7c48e5957ee3606ba79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107118"
---
# <a name="systemparameterscachesize-property"></a>SystemParameters. CacheSize, свойство

Возвращает или задает размер кэша базы данных на страницах. По умолчанию кэш базы данных автоматически настраивает свой размер, а установка этого свойства в ненулевое значение приводит к тому, что кэш подстраивается к целевому размеру.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Property CacheSize As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.CacheSize

SystemParameters.CacheSize = value
```

``` csharp
public static int CacheSize { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[SystemParameters - класс](./systemparameters-class.md)

[Элементы SystemParameters](./systemparameters-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
