---
description: 'Дополнительные сведения о свойстве: JET_COLUMNBASE. Кбмакс'
title: Свойство JET_COLUMNBASE. Кбмакс
TOCTitle: 'cbMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cbMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.cbmax(v=EXCHG.10)
ms:contentKeyID: 55103464
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cbMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.set_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.get_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cbMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b569f90546b9f07dc288e37422171c57cf5189ab047aec2afcecd14b37d1208e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781114"
---
# <a name="jet_columnbasecbmax-property"></a>Свойство JET_COLUMNBASE. Кбмакс

Возвращает максимальную длину столбца. Это имеет смысл только для столбцов типа [Text](./jet-coltyp-enumeration.md), [LongText](./jet-coltyp-enumeration.md), [binary](./jet-coltyp-enumeration.md) и [лонгбинари](./jet-coltyp-enumeration.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property cbMax As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNBASE
Dim value As Integer

value = instance.cbMax
```

``` csharp
public int cbMax { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс JET_COLUMNBASE](./jet-columnbase-class.md)

[Элементы JET_COLUMNBASE](./jet-columnbase-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
