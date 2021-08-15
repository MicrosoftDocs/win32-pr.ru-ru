---
description: 'Дополнительные сведения о: JET_LOGTIME. Метод ToDateTime'
title: JET_LOGTIME. Метод ToDateTime
TOCTitle: 'ToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime.todatetime(v=EXCHG.10)
ms:contentKeyID: 39512964
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: add66724ff34b3871462eef129dc6efd549159b39243a19565d4ca40d2f05b04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979854"
---
# <a name="jet_logtimetodatetime-method"></a>JET_LOGTIME. Метод ToDateTime

Создайте представление DateTime этого JET_LOGTIME.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Function ToDateTime As Nullable(Of DateTime)
'Usage
Dim instance As JET_LOGTIME
Dim returnValue As Nullable(Of DateTime)

returnValue = instance.ToDateTime()
```

``` csharp
public Nullable<DateTime> ToDateTime()
```

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\>  
Значение типа DateTime, представляющее JET_LOGTIME. Если JET_LOGTIME имеет значение null, возвращается значение null.  

#### <a name="implements"></a>Реализации

[IJET_LOGTIME. ToDateTime ()](./ijet-logtime.todatetime-method.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Структура JET_LOGTIME](./jet-logtime-structure2.md)

[Элементы JET_LOGTIME](./jet-logtime-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
