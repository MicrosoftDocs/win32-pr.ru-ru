---
description: 'Дополнительные сведения о свойстве: JET_INDEXLIST. Колумнидиколумн'
title: Свойство JET_INDEXLIST. Колумнидиколумн
TOCTitle: 'columnidiColumn property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidiColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidicolumn(v=EXCHG.10)
ms:contentKeyID: 55103664
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidiColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidiColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidiColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidiColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2759c04b60c15d5786306ec536c7eddb89b02172
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656657"
---
# <a name="jet_indexlistcolumnidicolumn-property"></a>Свойство JET_INDEXLIST. Колумнидиколумн

Возвращает значение columnid столбца во временной таблице, в котором хранится индекс этого столбца в ключе индекса. Столбец имеет тип [Long](./jet-coltyp-enumeration.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property columnidiColumn As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidiColumn
```

``` csharp
public JET_COLUMNID columnidiColumn { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_INDEXLIST](./jet-indexlist-class.md)

[Элементы JET_INDEXLIST](./jet-indexlist-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
