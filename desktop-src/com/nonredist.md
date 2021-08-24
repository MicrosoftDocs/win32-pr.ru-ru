---
title: нонредист
description: Добавляет имена в список файлов, которые не должны экспортироваться при упаковке приложений COM+ для установки на других компьютерах. Обратите внимание, что это подраздел, а не значение.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- COM-значение реестра НОНРЕДИСТ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b303c145ea48a51f72d6ee21078b5f29a6b6d4fabc7184d4a37e980a2bbb2e4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678464"
---
# <a name="nonredist"></a>нонредист

Добавляет имена в список файлов, которые не должны экспортироваться при упаковке приложений COM+ для установки на других компьютерах. Обратите внимание, что это подраздел, а не значение.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a>Remarks

Файлы, добавляемые в список, представлены парами «имя-значение», которые хранятся в этом разделе. В каждой паре «имя-значение» именем является имя файла, а значение зарезервировано.

 

 




