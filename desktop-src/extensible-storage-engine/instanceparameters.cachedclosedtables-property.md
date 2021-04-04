---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Качедклоседтаблес'
title: Инстанцепараметерс. Качедклоседтаблес, свойство
TOCTitle: 'CachedClosedTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55103293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CachedClosedTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CachedClosedTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f2465de2df3d25293f5298d40700512b6a086d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811632"
---
# <a name="instanceparameterscachedclosedtables-property"></a>Инстанцепараметерс. Качедклоседтаблес, свойство

Возвращает или задает значение, определяющее количество ресурсов дерева B +, кэшированных экземпляром после того, как таблицы, которые они представляют, были закрыты приложением. Большие значения для этого параметра приведут к тому, что ядро СУБД будет использовать больше памяти, но увеличит скорость, с которой приложение может случайно открыть большое количество таблиц. Это полезно для приложений, имеющих схему с очень большим количеством таблиц. Поддерживается в Windows Vista и выше. Игнорируется в Windows XP и Windows Server 2003.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property CachedClosedTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CachedClosedTables

instance.CachedClosedTables = value
```

``` csharp
public int CachedClosedTables { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Инстанцепараметерс](./instanceparameters-class.md)

[Элементы Инстанцепараметерс](./instanceparameters-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
