---
description: 'Дополнительные сведения о: JET_BKLOGTIME. Метод ToDateTime'
title: JET_BKLOGTIME. Метод ToDateTime
TOCTitle: 'ToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.ToDateTime
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.todatetime(v=EXCHG.10)
ms:contentKeyID: 39515201
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.ToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.ToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b6470e8486f5ff8c8ec8d1b7eb6678741fccc04f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344212"
---
# <a name="jet_bklogtimetodatetime-method"></a>JET_BKLOGTIME. Метод ToDateTime

Создайте представление DateTime этого JET_BKLOGTIME.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Function ToDateTime As Nullable(Of DateTime)
'Usage
Dim instance As JET_BKLOGTIME
Dim returnValue As Nullable(Of DateTime)

returnValue = instance.ToDateTime()
```

``` csharp
public Nullable<DateTime> ToDateTime()
```

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\>  
Значение типа DateTime, представляющее JET_BKLOGTIME. Если JET_BKLOGTIME имеет значение null, возвращается значение null.  

#### <a name="implements"></a>Реализации

[IJET_LOGTIME. ToDateTime ()](./ijet-logtime.todatetime-method.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_BKLOGTIME](./jet-bklogtime-structure2.md)

[Элементы JET_BKLOGTIME](./jet-bklogtime-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
