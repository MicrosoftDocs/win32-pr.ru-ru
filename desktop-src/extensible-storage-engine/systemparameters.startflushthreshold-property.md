---
description: 'Дополнительные сведения о свойстве: SystemParameters. Стартфлушсрешолд'
title: SystemParameters. Стартфлушсрешолд, свойство
TOCTitle: 'StartFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.startflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104050
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StartFlushThreshold
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0e520682253d7a586c36366d229be59e014c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347972"
---
# <a name="systemparametersstartflushthreshold-property"></a>SystemParameters. Стартфлушсрешолд, свойство

Возвращает или задает пороговое значение, при котором кэш страниц базы данных начинает удалять страницы из кэша, чтобы освободить место для страниц, которые не кэшируются. Когда количество буферов страниц в кэше падает ниже этого порога, запускается фоновый процесс для пополнения пула доступных буферов. Это пороговое значение всегда относительно максимального размера кэша, установленного JET_paramCacheSizeMax. Это пороговое значение также должно быть меньше порога окончания, установленного JET_paramStopFlushThreshold. Высота расстояния начального порога определяет время отклика, которое должен иметь кэш страниц базы данных для создания доступных буферов до того, как приложение потребует их. При высоком пороговом значении запуска фоновому процессу будет больше времени на реагирование. Тем не менее, при высоком пороговом значении приостанавливается более высокий порог, что уменьшает эффективный размер кэша страниц базы данных.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Property StartFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StartFlushThreshold

SystemParameters.StartFlushThreshold = value
```

``` csharp
public static int StartFlushThreshold { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[SystemParameters - класс](./systemparameters-class.md)

[Элементы SystemParameters](./systemparameters-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
