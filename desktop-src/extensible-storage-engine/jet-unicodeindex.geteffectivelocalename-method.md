---
description: 'Дополнительные сведения о: JET_UNICODEINDEX. Метод Жетеффективелокаленаме'
title: JET_UNICODEINDEX. Метод Жетеффективелокаленаме
TOCTitle: 'GetEffectiveLocaleName method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_unicodeindex.geteffectivelocalename(v=EXCHG.10)
ms:contentKeyID: 55103988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10932398e022701b76be19c3ea7949ce4cfd45b5a159ae5362e7f0e6a0e427bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979084"
---
# <a name="jet_unicodeindexgeteffectivelocalename-method"></a>JET_UNICODEINDEX. Метод Жетеффективелокаленаме

В качестве обходного решения для систем, которые не поддерживают код языка, мы преобразуем очень ограниченное число LCID в имена языковых стандартов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Function GetEffectiveLocaleName As String
'Usage
Dim instance As JET_UNICODEINDEX
Dim returnValue As String

returnValue = instance.GetEffectiveLocaleName()
```

``` csharp
public string GetEffectiveLocaleName()
```

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. String](/dotnet/api/system.string)  
Имя локали в стиле BCP-47.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_UNICODEINDEX](./jet-unicodeindex-class.md)

[Элементы JET_UNICODEINDEX](./jet-unicodeindex-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
