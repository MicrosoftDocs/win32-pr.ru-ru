---
description: 'Дополнительные сведения о свойстве: JET_INDEXLIST. Колумнидлкмапфлагс'
title: Свойство JET_INDEXLIST. Колумнидлкмапфлагс
TOCTitle: 'columnidLCMapFlags property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLCMapFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55103667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidLCMapFlags
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidLCMapFlags
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLCMapFlags
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2efdab9e48ad578b7a737479d2171b8d3f08599b8161deb238d7e3c5a0d9d877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118485656"
---
# <a name="jet_indexlistcolumnidlcmapflags-property"></a>Свойство JET_INDEXLIST. Колумнидлкмапфлагс

Возвращает значение columnid столбца во временной таблице, в котором хранятся флаги нормализации Юникода для индекса. Столбец имеет тип [Long](./jet-coltyp-enumeration.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property columnidLCMapFlags As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidLCMapFlags
```

``` csharp
public JET_COLUMNID columnidLCMapFlags { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_INDEXLIST](./jet-indexlist-class.md)

[Элементы JET_INDEXLIST](./jet-indexlist-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
