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
# <a name="how-to-define-extended-verbs"></a><span data-ttu-id="d940a-104">Определение расширенных команд</span><span class="sxs-lookup"><span data-stu-id="d940a-104">How to Define Extended Verbs</span></span>

<span data-ttu-id="d940a-105">С помощью реестра можно определить одну или несколько расширенных команд.</span><span class="sxs-lookup"><span data-stu-id="d940a-105">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="d940a-106">Связанные команды будут отображаться только в том случае, если пользователь щелкнет правой кнопкой мыши объект, удерживая нажатой клавишу SHIFT.</span><span class="sxs-lookup"><span data-stu-id="d940a-106">The associated commands will be displayed only when the user right-clicks an object while pressing the SHIFT key.</span></span>

## <a name="instructions"></a><span data-ttu-id="d940a-107">Инструкции</span><span class="sxs-lookup"><span data-stu-id="d940a-107">Instructions</span></span>


<span data-ttu-id="d940a-108">Чтобы определить команду как расширенную, просто добавьте расширенное значение **reg \_ SZ** в подраздел команды.</span><span class="sxs-lookup"><span data-stu-id="d940a-108">To define a verb as extended, simply add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="d940a-109">С этим значением не должно быть связано никаких данных.</span><span class="sxs-lookup"><span data-stu-id="d940a-109">The value should not have any data associated with it.</span></span> <span data-ttu-id="d940a-110">В следующем примере записи реестра показан пример из предыдущего раздела с параметром "доит", определенным в качестве расширенной команды.</span><span class="sxs-lookup"><span data-stu-id="d940a-110">The following sample registry entry shows the example from the previous section, with "doit" defined as an extended verb.</span></span>

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

 

 



