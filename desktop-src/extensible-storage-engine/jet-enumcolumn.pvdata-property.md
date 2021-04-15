---
description: 'Дополнительные сведения о свойстве: JET_ENUMCOLUMN. Пвдата'
title: Свойство JET_ENUMCOLUMN. Пвдата
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103500
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7d4c72a45d90fd8004af2011f9f6081a59cfabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497421"
---
# <a name="jet_enumcolumnpvdata-property"></a>Свойство JET_ENUMCOLUMN. Пвдата

Возвращает значение, перечисленное для столбца. Этот элемент используется, только если [Err](./jet-enumcolumn.err-property.md) равен [колумнсинглевалуе](./jet-wrn-enumeration.md). Это указывает на память, выделенную с помощью обратного вызова [JET_PFNREALLOC](./jet-pfnrealloc-delegate.md) распределителя, переданного в [жетенумератеколумнс (JET_SESID, JET_TABLEID, Int32, \[ \] , Int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, енумератеколумнсгрбит)](./api.jetenumeratecolumns-method.md). Не забудьте освободить память по завершении.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property pvData As IntPtr
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As IntPtr

value = instance.pvData
```

``` csharp
public IntPtr pvData { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. IntPtr](/dotnet/api/system.intptr)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_ENUMCOLUMN](./jet-enumcolumn-class.md)

[Элементы JET_ENUMCOLUMN](./jet-enumcolumn-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
