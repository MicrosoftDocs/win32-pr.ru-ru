---
description: 'Дополнительные сведения о: JET_RECPOS. Метод Контентекуалс'
title: JET_RECPOS. Метод Контентекуалс
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_RECPOS.ContentEquals(Microsoft.Isam.Esent.Interop.JET_RECPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recpos.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103845
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RECPOS.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RECPOS.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cff822551bd2687308dde12df1f4e0e381f58046
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911448"
---
# <a name="jet_recposcontentequals-method"></a>JET_RECPOS. Метод Контентекуалс

Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_RECPOS _
) As Boolean
'Usage
Dim instance As JET_RECPOS
Dim other As JET_RECPOS
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_RECPOS other
)
```

#### <a name="parameters"></a>Параметры

  - др.  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_RECPOS](./jet-recpos-class.md)  
    
    Экземпляр, сравниваемый с этим экземпляром.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если два экземпляра равны.  

#### <a name="implements"></a>Реализации

[Иконтентекуатабле \<T\> . Контентекуалс (T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_RECPOS](./jet-recpos-class.md)

[Элементы JET_RECPOS](./jet-recpos-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
