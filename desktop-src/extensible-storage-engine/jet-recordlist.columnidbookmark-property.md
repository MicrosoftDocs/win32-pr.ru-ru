---
description: 'Дополнительные сведения о свойстве: JET_RECORDLIST. Колумнидбукмарк'
title: Свойство JET_RECORDLIST. Колумнидбукмарк
TOCTitle: 'columnidBookmark property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recordlist.columnidbookmark(v=EXCHG.10)
ms:contentKeyID: 55103827
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.get_columnidBookmark
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.set_columnidBookmark
- Microsoft.Isam.Esent.Interop.JET_RECORDLIST.columnidBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0122462a3d809b59e4b3b17d5ecf82e342fac06267da7aae2875407b69b44deb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730414"
---
# <a name="jet_recordlistcolumnidbookmark-property"></a>Свойство JET_RECORDLIST. Колумнидбукмарк

Возвращает значение columnid столбца во временной таблице, в котором хранится закладка записи. Столбец имеет тип JET_coltyp. Полнотекстовым.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property columnidBookmark As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_RECORDLIST
Dim value As JET_COLUMNID

value = instance.columnidBookmark
```

``` csharp
public JET_COLUMNID columnidBookmark { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс JET_RECORDLIST](./jet-recordlist-class.md)

[Элементы JET_RECORDLIST](./jet-recordlist-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
