---
description: 'Дополнительные сведения о: JET_CONDITIONALCOLUMN. Метод Контентекуалс'
title: JET_CONDITIONALCOLUMN. Метод Контентекуалс
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN.ContentEquals(Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_conditionalcolumn.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103531
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ed50b5951cb255fcdc21854df6bcd0a3865e8efc54f8d9587454c3abc434b9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118766561"
---
# <a name="jet_conditionalcolumncontentequals-method"></a>JET_CONDITIONALCOLUMN. Метод Контентекуалс

Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_CONDITIONALCOLUMN _
) As Boolean
'Usage
Dim instance As JET_CONDITIONALCOLUMN
Dim other As JET_CONDITIONALCOLUMN
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_CONDITIONALCOLUMN other
)
```

#### <a name="parameters"></a>Параметры

  - др.  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-class.md)  
    
    Экземпляр, сравниваемый с этим экземпляром.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если два экземпляра равны.  

#### <a name="implements"></a>Реализации

[Иконтентекуатабле \<T\> . Контентекуалс (T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-class.md)

[Элементы JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
