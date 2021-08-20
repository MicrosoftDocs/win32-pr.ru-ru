---
description: 'Дополнительные сведения о свойстве: JET_UNICODEINDEX. Двмапфлагс'
title: Свойство JET_UNICODEINDEX. Двмапфлагс
TOCTitle: 'dwMapFlags property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.dwMapFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_unicodeindex.dwmapflags(v=EXCHG.10)
ms:contentKeyID: 55103990
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.dwMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.set_dwMapFlags
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.get_dwMapFlags
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.dwMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7e7f7be15a52948a269544b606d90a290f129ff262240ddc92e33a67c9b24fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117892119"
---
# <a name="jet_unicodeindexdwmapflags-property"></a>Свойство JET_UNICODEINDEX. Двмапфлагс

Возвращает или задает флаги, используемые с LCMapString завершилось ошибкой при нормализации данных в Юникоде.

Этот API несовместим с CLS. 

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Property dwMapFlags As UInteger
    Get
    Set
'Usage
Dim instance As JET_UNICODEINDEX
Dim value As UInteger

value = instance.dwMapFlags

instance.dwMapFlags = value
```

``` csharp
[CLSCompliantAttribute(false)]
public uint dwMapFlags { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. UInt32](/dotnet/api/system.uint32)  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс JET_UNICODEINDEX](./jet-unicodeindex-class.md)

[Элементы JET_UNICODEINDEX](./jet-unicodeindex-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
