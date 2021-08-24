---
description: 'Дополнительные сведения о: Вистагрбитс. Индекскросспродукт поле'
title: Поле Вистагрбитс. Индекскросспродукт (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: IndexCrossProduct field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexcrossproduct(v=EXCHG.10)
ms:contentKeyID: 55104426
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad3828411177d1c500c1b21b62797f093143ba1ac5b9770d9d6444d5c1a7aa9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471134"
---
# <a name="vistagrbitsindexcrossproduct-field"></a>Вистагрбитс. Индекскросспродукт, поле

Если задать этот флаг для индекса, имеющего более одного ключевого столбца, который является многозначным, будет создана запись индекса для каждого результата перекрестного произведения всех значений в этих ключевых столбцах. В противном случае индекс будет иметь только одну запись для каждого многозначного ключевого столбца, который является многозначным столбцом, и каждая из этих элементов индекса будет использовать первое Многозначное значение из любых других ключевых столбцов, которые являются многозначными столбцами. Например, если вы указали этот флаг для индекса по столбцу A, который имеет значения "Red" и "Blue", а столбец B имеет значения "1" и "2", то будут созданы следующие элементы индекса: "Red", "1"; "Red", "2"; "Blue", "1"; "Blue", "2". В противном случае будут созданы следующие записи индекса: "Red", "1"; "Blue", "1".

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Const IndexCrossProduct As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexCrossProduct
```

``` csharp
public const CreateIndexGrbit IndexCrossProduct
```

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Вистагрбитс](./vistagrbits-class.md)

[Элементы Вистагрбитс](./vistagrbits-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
