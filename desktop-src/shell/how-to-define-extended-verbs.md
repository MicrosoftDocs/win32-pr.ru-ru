---
description: С помощью реестра можно определить одну или несколько расширенных команд. Связанные команды будут отображаться только в том случае, если пользователь щелкнет правой кнопкой мыши объект, удерживая нажатой клавишу SHIFT.
ms.assetid: C6E51716-1D4F-454F-9AF4-8D0E486CB885
title: Определение расширенных команд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4bd8cca04b40bb0b0b77bab5fd7546fd5bff45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985449"
---
# <a name="how-to-define-extended-verbs"></a>Определение расширенных команд

С помощью реестра можно определить одну или несколько расширенных команд. Связанные команды будут отображаться только в том случае, если пользователь щелкнет правой кнопкой мыши объект, удерживая нажатой клавишу SHIFT.

## <a name="instructions"></a>Инструкции


Чтобы определить команду как расширенную, просто добавьте расширенное значение **reg \_ SZ** в подраздел команды. С этим значением не должно быть связано никаких данных. В следующем примере записи реестра показан пример из предыдущего раздела с параметром "доит", определенным в качестве расширенной команды.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            extended
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 



