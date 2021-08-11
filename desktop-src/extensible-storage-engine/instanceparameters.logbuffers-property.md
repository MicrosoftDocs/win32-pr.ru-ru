---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Логбуфферс'
title: Инстанцепараметерс. Логбуфферс, свойство
TOCTitle: 'LogBuffers property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logbuffers(v=EXCHG.10)
ms:contentKeyID: 55107472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogBuffers
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60fbf06d13a8252051830c9a91dd348c2a7295a63212b587bfac9905b3b5903a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118255965"
---
# <a name="instanceparameterslogbuffers-property"></a>Инстанцепараметерс. Логбуфферс, свойство

Возвращает или задает объем памяти, используемый для кэширования записей журнала до их записи в файл журнала транзакций. Единицей для этого параметра является размер сектора тома, содержащего файлы журнала транзакций. Размер сектора почти всегда 512 байт, поэтому можно считать, что размер для единицы является надежным. Этот параметр влияет на производительность. Когда ядро СУБД находится в режиме высокой нагрузки на обновление, этот буфер может быстро стать полностью загруженным. Больший размер кэша для файла журнала транзакций очень важен для хорошего уровня производительности при такой высокой нагрузке. Значение по умолчанию для этого случая известно слишком мало. Не устанавливайте для этого параметра количество буферов большего размера (в байтах), чем размер файла журнала транзакций, превышающий половину.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property LogBuffers As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogBuffers

instance.LogBuffers = value
```

``` csharp
public int LogBuffers { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Инстанцепараметерс](./instanceparameters-class.md)

[Элементы Инстанцепараметерс](./instanceparameters-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
