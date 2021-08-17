---
description: 'Дополнительные сведения о свойстве: Есентстопватч. Среадстатс'
title: Есентстопватч. Среадстатс, свойство
TOCTitle: 'ThreadStats property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch.threadstats(v=EXCHG.10)
ms:contentKeyID: 55102996
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStopwatch.get_ThreadStats
- Microsoft.Isam.Esent.Interop.EsentStopwatch.set_ThreadStats
- Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13cfe4ac7f318530e7fee60d0b0020c94602f5ad1a1dd1ba4f262a25380b7409
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119273104"
---
# <a name="esentstopwatchthreadstats-property"></a>Есентстопватч. Среадстатс, свойство

Возвращает суммарную статистику объема работ ESENT, измеренную текущим экземпляром.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property ThreadStats As JET_THREADSTATS
    Get
    Private Set
'Usage
Dim instance As EsentStopwatch
Dim value As JET_THREADSTATS

value = instance.ThreadStats
```

``` csharp
public JET_THREADSTATS ThreadStats { get; private set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Есентстопватч](./esentstopwatch-class.md)

[Элементы Есентстопватч](./esentstopwatch-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
