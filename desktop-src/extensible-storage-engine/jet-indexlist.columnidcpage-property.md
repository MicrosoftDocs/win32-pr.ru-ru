---
description: 'Дополнительные сведения о свойстве: JET_INDEXLIST. Колумнидкпаже'
title: Свойство JET_INDEXLIST. Колумнидкпаже
TOCTitle: 'columnidcPage property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcPage
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidcpage(v=EXCHG.10)
ms:contentKeyID: 55103616
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcPage
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcPage
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcPage
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcPage
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 969562ad81147178470e531da0cb1669e32709f3624c4d25fe5ea7f6bce68e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119109819"
---
# <a name="jet_indexlistcolumnidcpage-property"></a>Свойство JET_INDEXLIST. Колумнидкпаже

Возвращает значение columnid столбца во временной таблице, в котором хранится количество страниц в индексе. Это значение не является текущим и обновляется только с помощью "API. Жеткомпутестатс". Столбец имеет тип [Long](./jet-coltyp-enumeration.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property columnidcPage As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcPage
```

``` csharp
public JET_COLUMNID columnidcPage { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_INDEXLIST](./jet-indexlist-class.md)

[Элементы JET_INDEXLIST](./jet-indexlist-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
