---
title: Протокол
description: Указывает, что этот класс OLE 2 может быть вставлен в контейнеры OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Раздел реестра протокола COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7721e4f90a122fcbc519163d80c1e8e549f2b6aa05526d33d9693783abd1276a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130026"
---
# <a name="protocol"></a>Протокол

Указывает, что этот класс OLE 2 может быть вставлен в контейнеры OLE 1.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Protocol
         StdFileEditing
            Server = path
            Verb
               0 = verb1
               1 = verb2
               ...
```

## <a name="remarks"></a>Remarks

Запись **стдфилидитинг** указывает сведения о совместимости OLE 1. Он должен присутствовать только в том случае, если объекты этого класса можно вставлять в контейнеры OLE 1.

**Server** указывает полный путь к приложению сервера OLE 2, а **глагол** задает команды. Глагол 0 является первичной командой, а дополнительные команды должны быть пронумерованы последовательно.

 

 




