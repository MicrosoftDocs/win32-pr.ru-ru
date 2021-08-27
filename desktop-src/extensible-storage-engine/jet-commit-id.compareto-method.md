---
description: Дополнительные сведения о методе JET_COMMIT_ID. CompareTo
title: Метод JET_COMMIT_ID. CompareTo (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.CompareTo(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.compareto(v=EXCHG.10)
ms:contentKeyID: 55104397
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.CompareTo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a101cd38eb80598f907068d8fd27d2217ad73db1476dc41d42b2a6caaae3e6ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118766902"
---
# <a name="jet_commit_idcompareto-method"></a>JET_COMMIT_ID. CompareTo, метод

Возвращает значение, сравнивающее данный экземпляр с другим.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_COMMIT_ID _
) As Integer
'Usage
Dim instance As JET_COMMIT_ID
Dim other As JET_COMMIT_ID
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_COMMIT_ID other
)
```

#### <a name="parameters"></a>Параметры

  - др.  
    Тип: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)  
    
    Экземпляр, сравниваемый с этим экземпляром.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Int32](/dotnet/api/system.int32)  
Значение со знаком, представляющее относительное положение экземпляров.  

#### <a name="implements"></a>Реализации

[Интерфейс IComparable \<T\> . CompareTo (T)](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_COMMIT_ID](./jet-commit-id-class.md)

[Элементы JET_COMMIT_ID](./jet-commit-id-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
