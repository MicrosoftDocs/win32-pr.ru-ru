---
description: 'Дополнительные сведения: структура JET_BKINFO'
title: Структура JET_BKINFO
TOCTitle: JET_BKINFO structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_BKINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bkinfo(v=EXCHG.10)
ms:contentKeyID: 39511166
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKINFO
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKINFO
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e7e309704bce5ba0d4cba82494205cb92a0d904ef258a335d4858e337bcd884
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118767361"
---
# <a name="jet_bkinfo-structure"></a>Структура JET_BKINFO

Содержит коллекцию данных о конкретном событии резервного копирования.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_BKINFO _
    Implements IEquatable(Of JET_BKINFO), INullableJetStruct
'Usage
Dim instance As JET_BKINFO
```

``` csharp
[SerializableAttribute]
public struct JET_BKINFO : IEquatable<JET_BKINFO>, 
    INullableJetStruct
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы JET_BKINFO](./jet-bkinfo-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
