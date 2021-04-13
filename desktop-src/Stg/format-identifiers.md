---
title: Идентификаторы формата
description: Значения набора свойств хранятся в разделе, помеченном уникальным FMTID.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Идентификаторы формата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0202cd1287c3b4fef6e9e2b56e272541a03425b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329544"
---
# <a name="format-identifiers"></a>Идентификаторы формата

Значения набора свойств хранятся в разделе, помеченном уникальным FMTID. Например, FMTID для набора свойств "Сводная информация COM" — **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.

Чтобы определить FMTID для набора свойств сводных данных, используйте макрос **define \_ GUID** в включаемом файле для кода, который управляет набором свойств.


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



Любой код, который требует FMTID для набора свойств сводки, может получить доступ к нему через переменную *FMTID \_ SummaryInformation* .

При хранении наборов свойств в экземплярах [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) преобразуйте FMTID в строковое имя для объекта хранилища.

 

 




