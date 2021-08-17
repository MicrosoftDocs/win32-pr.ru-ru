---
description: 'Дополнительные сведения о методе: reкомпареоптионсфромлкмапфлагсs.'
title: Метод преобразования. Компареоптионсфромлкмапфлагс
TOCTitle: 'CompareOptionsFromLCMapFlags method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags(System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.compareoptionsfromlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55100975
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bfe3a65c52d23ee335a81560775f0063b8ca81a10cc43c1787e353a5b803eed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117901850"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a>Метод преобразования. Компареоптионсфромлкмапфлагс

Заданными флагами для Лкмапфлагс, преобразуйте их в параметры сравнения. Неизвестные параметры игнорируются.

Этот API несовместим с CLS. 

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function CompareOptionsFromLCMapFlags ( _
    lcmapFlags As UInteger _
) As CompareOptions
'Usage
Dim lcmapFlags As UInteger
Dim returnValue As CompareOptions

returnValue = Conversions.CompareOptionsFromLCMapFlags(lcmapFlags)
```

``` csharp
[CLSCompliantAttribute(false)]
public static CompareOptions CompareOptionsFromLCMapFlags(
    uint lcmapFlags
)
```

#### <a name="parameters"></a>Параметры

  - лкмапфлагс  
    Тип: [System. UInt32](/dotnet/api/system.uint32)  
    
    Флаги LCMapString завершилось ошибкой.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)  
CompareOptions, описывающий флаги (известные).  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс преобразований](./conversions-class.md)

[Преобразования элементов](./conversions-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
