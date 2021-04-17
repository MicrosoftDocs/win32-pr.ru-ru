---
description: 'Дополнительные сведения о методе: reлкмапфлагсфромкомпареоптионсs.'
title: Метод преобразования. Лкмапфлагсфромкомпареоптионс
TOCTitle: 'LCMapFlagsFromCompareOptions method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions(System.Globalization.CompareOptions)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.lcmapflagsfromcompareoptions(v=EXCHG.10)
ms:contentKeyID: 55100974
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55c034bb0e4e48217c5294d83f65b48245a5e455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711321"
---
# <a name="conversionslcmapflagsfromcompareoptions-method"></a>Метод преобразования. Лкмапфлагсфромкомпареоптионс

Дайте CompareOptions, преобразуйте их в флаги из LCMapString завершилось ошибкой. Неизвестные параметры игнорируются.

Этот API несовместим с CLS. 

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function LCMapFlagsFromCompareOptions ( _
    compareOptions As CompareOptions _
) As UInteger
'Usage
Dim compareOptions As CompareOptions
Dim returnValue As UInteger

returnValue = Conversions.LCMapFlagsFromCompareOptions(compareOptions)
```

``` csharp
[CLSCompliantAttribute(false)]
public static uint LCMapFlagsFromCompareOptions(
    CompareOptions compareOptions
)
```

#### <a name="parameters"></a>Параметры

  - compareOptions  
    Тип: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)  
    
    Преобразуемые параметры.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. UInt32](/dotnet/api/system.uint32)  
Флаги LCMapString завершилось ошибкой, соответствующие параметрам сравнения. Неподдерживаемые параметры игнорируются.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс преобразований](./conversions-class.md)

[Преобразования элементов](./conversions-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
