---
description: 'Дополнительные сведения о свойстве: JET_ENUMCOLUMNID. Ргтагсекуенце'
title: Свойство JET_ENUMCOLUMNID. Ргтагсекуенце
TOCTitle: 'rgtagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.rgtagsequence(v=EXCHG.10)
ms:contentKeyID: 55103529
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d61d69fb9f22a31f07ee2eb0b4116a13761d961
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808543"
---
# <a name="jet_enumcolumnidrgtagsequence-property"></a>Свойство JET_ENUMCOLUMNID. Ргтагсекуенце

Возвращает или задает массив индексов, отсчитываемый от единицы, в массиве значений столбцов для данного столбца. Единственный элемент — это Итагсекуенце, который определен в JET_RETRIEVECOLUMN. Итагсекуенце 0 (ноль) означает "Skip". Итагсекуенце 1 означает возврат значения первого столбца столбца, 2 — второй и т. д.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property rgtagSequence As Integer()
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer()

value = instance.rgtagSequence

instance.rgtagSequence = value
```

``` csharp
public int[] rgtagSequence { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип \[\]  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md)

[Элементы JET_ENUMCOLUMNID](./jet-enumcolumnid-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
