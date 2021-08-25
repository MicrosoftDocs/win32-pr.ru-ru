---
description: Дополнительные сведения о методе API. Жетрестореинстанце
title: API. Жетрестореинстанце, метод
TOCTitle: 'JetRestoreInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrestoreinstance(v=EXCHG.10)
ms:contentKeyID: 55100787
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3fef9ca38f8e8efb86813666840f859ed10287197d5f3b6ed0bafdd434ea43dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947774"
---
# <a name="apijetrestoreinstance-method"></a>API. Жетрестореинстанце, метод

Восстанавливает и восстанавливает потоковую передачу резервной копии экземпляра, включая все подключенные базы данных. Он предназначен для работы с резервной копией, созданной с помощью функции [жетбаккупинстанце (JET_INSTANCE, String, баккупгрбит, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) . Это самая простая и наиболее функциональная функция Restore.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetRestoreInstance ( _
    instance As JET_INSTANCE, _
    source As String, _
    destination As String, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim source As String
Dim destination As String
Dim statusCallback As JET_PFNSTATUSApi.JetRestoreInstance(instance, _
    source, destination, statusCallback)
```

``` csharp
public static void JetRestoreInstance(
    JET_INSTANCE instance,
    string source,
    string destination,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a>Параметры

  - экземпляр  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Используемый экземпляр. Экземпляр не должен инициализироваться. При восстановлении файлов экземпляр будет инициализирован.

<!-- end list -->

  - source  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Расположение резервной копии. Резервная копия должна быть создана с помощью [жетбаккупинстанце (JET_INSTANCE, String, баккупгрбит, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).

<!-- end list -->

  - ресурс destination  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Имя папки, в которую будут копироваться и восстанавливаться файлы базы данных из набора резервных копий. Если задано значение null, файлы базы данных будут скопированы и восстановлены в исходном расположении.

<!-- end list -->

  - статускаллбакк  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Необязательный обратный вызов уведомления о состоянии.

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
