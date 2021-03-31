---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Клеанупмисматчедлогфилес'
title: Инстанцепараметерс. Клеанупмисматчедлогфилес, свойство
TOCTitle: 'CleanupMismatchedLogFiles property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cleanupmismatchedlogfiles(v=EXCHG.10)
ms:contentKeyID: 55103296
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e80bb8877335e26cb233a09b2fa3ec3a6f12615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155403"
---
# <a name="instanceparameterscleanupmismatchedlogfiles-property"></a>Инстанцепараметерс. Клеанупмисматчедлогфилес, свойство

Возвращает или задает значение, указывающее, завершается ли Жетинит сбоем, когда ядро СУБД настроено для начала использования файлов журнала транзакций на диске, размер которых отличается от настроенного. Обычно [жетинит (JET_INSTANCE)](./api.jetinit-method.md) успешно восстановит базы данных, но завершится с ошибкой [логфилесиземисматчдатабасесконсистент](./jet-err-enumeration.md) , чтобы указать, что размер файла журнала настроен неправильно. Однако если этот параметр имеет значение true, то ядро СУБД автоматически удалит все старые файлы журналов, а затем запустит новый набор файлов журнала транзакций, используя настроенный размер файла журнала. Этот параметр полезен, когда приложению требуется прозрачно изменить размер файла журнала транзакций, но все равно работать прозрачно в сценариях обновления и восстановления.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property CleanupMismatchedLogFiles As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CleanupMismatchedLogFiles

instance.CleanupMismatchedLogFiles = value
```

``` csharp
public bool CleanupMismatchedLogFiles { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Инстанцепараметерс](./instanceparameters-class.md)

[Элементы Инстанцепараметерс](./instanceparameters-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
