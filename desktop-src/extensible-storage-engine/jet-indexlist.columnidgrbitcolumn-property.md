---
description: 'Дополнительные сведения о свойстве: JET_INDEXLIST. Колумнидгрбитколумн'
title: Свойство JET_INDEXLIST. Колумнидгрбитколумн
TOCTitle: 'columnidgrbitColumn property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidgrbitcolumn(v=EXCHG.10)
ms:contentKeyID: 55103665
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidgrbitColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidgrbitColumn
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidgrbitColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8588b5e7647507eb417610baab685e27e9c00a836f56ed6f1da499b0b66121e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038962"
---
# <a name="jet_indexlistcolumnidgrbitcolumn-property"></a>Свойство JET_INDEXLIST. Колумнидгрбитколумн

Возвращает значение columnid столбца во временной таблице, в котором хранится грбит, применяемый к индексированному столбцу. См. [индекскэйгрбит](./indexkeygrbit-enumeration.md). Столбец имеет тип [Long](./jet-coltyp-enumeration.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property columnidgrbitColumn As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidgrbitColumn
```

``` csharp
public JET_COLUMNID columnidgrbitColumn { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс JET_INDEXLIST](./jet-indexlist-class.md)

[Элементы JET_INDEXLIST](./jet-indexlist-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
