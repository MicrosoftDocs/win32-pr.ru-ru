---
description: 'Дополнительные сведения о свойстве: JET_INDEXLIST. Колумнидкколумн'
title: Свойство JET_INDEXLIST. Колумнидкколумн
TOCTitle: 'columnidcColumn property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidccolumn(v=EXCHG.10)
ms:contentKeyID: 55103595
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d1c6ca59424680b050ce2480645bb6eb922534a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817169"
---
# <a name="jet_indexlistcolumnidccolumn-property"></a>Свойство JET_INDEXLIST. Колумнидкколумн

Возвращает значение columnid столбца во временной таблице, в котором хранится количество столбцов в ключе индекса. Столбец имеет тип [Long](./jet-coltyp-enumeration.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property columnidcColumn As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcColumn
```

``` csharp
public JET_COLUMNID columnidcColumn { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_INDEXLIST](./jet-indexlist-class.md)

[Элементы JET_INDEXLIST](./jet-indexlist-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
