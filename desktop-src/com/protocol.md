---
title: Протокол
description: Указывает, что этот класс OLE 2 может быть вставлен в контейнеры OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Раздел реестра протокола COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710111"
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

## <a name="remarks"></a>Комментарии

Запись **стдфилидитинг** указывает сведения о совместимости OLE 1. Он должен присутствовать только в том случае, если объекты этого класса можно вставлять в контейнеры OLE 1.

**Server** указывает полный путь к приложению сервера OLE 2, а **глагол** задает команды. Глагол 0 является первичной командой, а дополнительные команды должны быть пронумерованы последовательно.

 

 




