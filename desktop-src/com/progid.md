---
title: 'ProgID:'
description: Связывает идентификатор ProgID с идентификатором CLSID.
ms.assetid: 89060943-7007-418b-a544-effbad548e87
keywords:
- Код COM раздела реестра ProgID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feec17db2cf16425968c64ef25759f284341bdb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775884"
---
# <a name="progid"></a>ProgID:

Связывает идентификатор ProgID с идентификатором CLSID.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ProgID = value
```

## <a name="remarks"></a>Комментарии

Каждый класс вставляемого объекта имеет идентификатор ProgID. Сведения о создании ProgID см. в разделе [ <ProgID> ключ](-progid--key.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[<ProgID> раздел](-progid--key.md)
</dt> <dt>

[**версиониндепендентпрогид**](versionindependentprogid.md)
</dt> </dl>

 

 




