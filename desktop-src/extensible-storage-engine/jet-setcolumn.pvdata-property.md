---
description: 'Дополнительные сведения о свойстве: JET_SETCOLUMN. Пвдата'
title: Свойство JET_SETCOLUMN. Пвдата
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103932
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.set_pvData
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.pvData
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c47170dd68749b13f0c6a3bc818f0a2fb775e77b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809022"
---
# <a name="jet_setcolumnpvdata-property"></a>Свойство JET_SETCOLUMN. Пвдата

Возвращает или задает указатель на данные, которые необходимо задать.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property pvData As Byte()
    Get
    Set
'Usage
Dim instance As JET_SETCOLUMN
Dim value As Byte()

value = instance.pvData

instance.pvData = value
```

``` csharp
public byte[] pvData { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип \[\]  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_SETCOLUMN](./jet-setcolumn-class.md)

[Элементы JET_SETCOLUMN](./jet-setcolumn-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
