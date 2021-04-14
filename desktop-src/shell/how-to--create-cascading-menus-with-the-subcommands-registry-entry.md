---
description: В Windows 7 и более поздних версиях можно использовать запись подкоманд в реестре для создания каскадных меню с помощью процедуры, приведенной в этом разделе.
title: Создание каскадных меню с записью реестра "подкоманды"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b1168daae5ea927f079c66eb436c099f8b3d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997714"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a>Создание каскадных меню с помощью записи реестра "подкоманды"

В Windows 7 и более поздних версиях можно использовать запись подкоманд в реестре для создания каскадных меню с помощью процедуры, приведенной в этом разделе.

## <a name="instructions"></a>Инструкции

### <a name="step-1"></a>Шаг 1.

Создайте новый подраздел в разделе **\_ классы hKey \_ root** \\ *ProgID* \\ **Shell**, где *ProgID* — это тип файла, для которого необходимо добавить каскадное меню. Этот новый подраздел можно назвать любым нужным образом. В оставшейся части этого раздела мы назовем его *каскадемену*, как показано в следующем примере.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a>Шаг 2.

Добавьте запись с именем "Муиверб" типа **reg \_ SZ** или **reg \_ expand \_ SZ** в подраздел *каскадемену* . Назначьте этой записи строковое значение, например "проверить каскадное меню". Как правило, эта строка предоставляется в виде ссылки на ресурс в виде " @file , ресурса". Значение (по умолчанию) для подраздела *каскадемену* не должно быть задано.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a>Шаг 3.

Добавьте в подраздел *каскадемену* запись с именем "подкоманды", введите **reg \_ SZ** или **reg \_ expand \_ SZ**. Присвойте этой записи разделенный точками с запятой список команд, которые должны отображаться в меню в нужном порядке их отображения.

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a>Шаг 4.

Заполните подраздел **коммандсторе** с реализацией глаголов для любых методов реализации пользовательских статических глаголов, которые использовались в записи подкоманд. Например:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  CommandStore
                     Shell
                        VerbName
                           command
                              (Default) = notepad.exe %1
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание статических каскадных меню](creating-static-cascading-menus.md)
</dt> </dl>

 

 



