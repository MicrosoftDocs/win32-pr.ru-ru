---
description: 'Дополнительные сведения о свойстве: JET_INDEXLIST. Колумнидлангид'
title: Свойство JET_INDEXLIST. Колумнидлангид
TOCTitle: 'columnidLangid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLangid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidlangid(v=EXCHG.10)
ms:contentKeyID: 55103666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLangid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidLangid
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidLangid
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidLangid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 934920cf41dd794c410588470bb694915da74469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683885"
---
# <a name="jet_indexlistcolumnidlangid-property"></a>Свойство JET_INDEXLIST. Колумнидлангид

Возвращает значение columnid столбца во временной таблице, в котором хранится идентификатор языка (LCID) индекса. Столбец имеет тип [Short](./jet-coltyp-enumeration.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property columnidLangid As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidLangid
```

``` csharp
public JET_COLUMNID columnidLangid { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_INDEXLIST](./jet-indexlist-class.md)

[Элементы JET_INDEXLIST](./jet-indexlist-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
