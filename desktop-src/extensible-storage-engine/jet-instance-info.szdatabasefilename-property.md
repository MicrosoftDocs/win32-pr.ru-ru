---
description: 'Дополнительные сведения о свойстве: JET_INSTANCE_INFO. Сздатабасефиленаме'
title: Свойство JET_INSTANCE_INFO. Сздатабасефиленаме
TOCTitle: 'szDatabaseFileName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.szdatabasefilename(v=EXCHG.10)
ms:contentKeyID: 55103711
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.get_szDatabaseFileName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55414184fd25a90f3fbb57be8fb5d84264fde5dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684430"
---
# <a name="jet_instance_infoszdatabasefilename-property"></a>Свойство JET_INSTANCE_INFO. Сздатабасефиленаме

Возвращает коллекцию строк, содержащую имя файла базы данных, присоединенной к экземпляру базы данных. Массив содержит элементы cDatabase.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public ReadOnly Property szDatabaseFileName As IList(Of String)
    Get
'Usage
Dim instance As JET_INSTANCE_INFO
Dim value As IList(Of String)

value = instance.szDatabaseFileName
```

``` csharp
public IList<string> szDatabaseFileName { get; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Collections. Generic. IList](/dotnet/api/system.collections.generic.ilist-1)\<[String](/dotnet/api/system.string)\>  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_INSTANCE_INFO](./jet-instance-info-class.md)

[Элементы JET_INSTANCE_INFO](./jet-instance-info-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
