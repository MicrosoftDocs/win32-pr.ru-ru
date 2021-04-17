---
title: Interface (COM)
description: Необязательная запись, указывающая все идентификаторы интерфейса (идентификаторов IID), поддерживаемые связанным классом.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- Раздел реестра интерфейса COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990c06285d60067c9a26faffabffc70cbdd283d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105710430"
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

## <a name="remarks"></a>Комментарии

Если имя интерфейса отсутствует в этом списке, интерфейс не может поддерживаться экземпляром этого класса.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ключ интерфейса](interface-key.md)
</dt> </dl>

 

 




