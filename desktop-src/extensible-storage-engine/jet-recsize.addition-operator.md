---
description: 'Дополнительные сведения о: JET_RECSIZE. Оператор сложения'
title: JET_RECSIZE. Оператор сложения (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Addition operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_addition(v=EXCHG.10)
ms:contentKeyID: 39512451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Addition
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Addition
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c675e0b7fffc00f181bc56f314ddcbbdac56c9c910abbaa0f88f69ad321bce2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890394"
---
# <a name="jet_recsizeaddition-operator"></a>JET_RECSIZE. Оператор сложения

Добавьте размеры в две структуры JET_RECSIZE.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Operator + ( _
    left As JET_RECSIZE, _
    right As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim left As JET_RECSIZE
Dim right As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = (left + right)
```

``` csharp
public static JET_RECSIZE operator +(
    JET_RECSIZE left,
    JET_RECSIZE right
)
```

#### <a name="parameters"></a>Параметры

  - Левое  
    Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    Первый JET_RECSIZE.

<!-- end list -->

  - right  
    Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    Второй JET_RECSIZE.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
JET_RECSIZE, содержащий результат сложения размеров слева и справа.  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Структура JET_RECSIZE](./jet-recsize-structure2.md)

[Элементы JET_RECSIZE](./jet-recsize-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
