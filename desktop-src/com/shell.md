---
title: Оболочка (COM)
description: Предоставляет данные для печати оболочки Windows 3,1 и открытия файлов.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- COM-сценарий раздела реестра оболочки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800659"
---
# <a name="shell-com"></a>Оболочка (COM)

Предоставляет данные для печати оболочки Windows 3,1 и **открытия файлов** .

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Shell
         Open
            command = path %1
         Print
            command = path %1
```

## <a name="remarks"></a>Remarks

Эти записи должны предоставить путь и имя файла приложения.

 

 




