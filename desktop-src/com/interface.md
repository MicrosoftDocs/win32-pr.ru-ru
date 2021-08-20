---
title: Interface (COM)
description: Необязательная запись, указывающая все идентификаторы интерфейса (идентификаторов IID), поддерживаемые связанным классом.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- Раздел реестра интерфейса COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d8eaa38b97896f623c8d9f245c48f8d12634f930dc193cba14d5a9217a261e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048122"
---
# <a name="interface-com"></a>Interface (COM)

Необязательная запись, указывающая все идентификаторы интерфейса (идентификаторов IID), поддерживаемые связанным классом.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a>Remarks

Если имя интерфейса отсутствует в этом списке, интерфейс не может поддерживаться экземпляром этого класса.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ключ интерфейса](interface-key.md)
</dt> </dl>

 

 




