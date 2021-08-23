---
description: 'Дополнительные сведения о: JET_TABLECREATE. Метод Контентекуалс'
title: JET_TABLECREATE. Метод Контентекуалс
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.ContentEquals(Microsoft.Isam.Esent.Interop.JET_TABLECREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103993
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 653aec23752d992059def6698b1d1eabadbdfc52d8988c047720648b844ebf70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979214"
---
# <a name="jet_tablecreatecontentequals-method"></a>JET_TABLECREATE. Метод Контентекуалс

Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_TABLECREATE _
) As Boolean
'Usage
Dim instance As JET_TABLECREATE
Dim other As JET_TABLECREATE
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_TABLECREATE other
)
```

#### <a name="parameters"></a>Параметры

  - др.  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)  
    
    Экземпляр, сравниваемый с этим экземпляром.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если два экземпляра равны.  

#### <a name="implements"></a>Реализации

[Иконтентекуатабле \<T\> . Контентекуалс (T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_TABLECREATE](./jet-tablecreate-class.md)

[Элементы JET_TABLECREATE](./jet-tablecreate-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
