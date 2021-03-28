---
description: В Windows 7 и более поздних версиях можно добавлять команды в папку с помощью Desktop.ini. Дополнительные сведения о Desktop.ini файлах см. в статье Настройка папок с помощью Desktop.ini.
ms.assetid: F03AB35D-FBFE-46C2-A37F-F70C18219B9A
title: Реализация пользовательских команд для папок с помощью Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133726133abe884863a0b4d2abc0cc76aab1310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985433"
---
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a>Реализация пользовательских команд для папок с помощью Desktop.ini

В Windows 7 и более поздних версиях можно добавлять команды в папку с помощью Desktop.ini. Дополнительные сведения о Desktop.ini файлах см. [в статье Настройка папок с помощью Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> Desktop.ini файлы всегда должны быть помечены как   +  **скрытые** системой, чтобы они не отображались для пользователей.

 

Чтобы добавить пользовательские команды для папок с помощью файла Desktop.ini, выполните следующие действия.

## <a name="instructions"></a>Инструкции

### <a name="step-1"></a>Шаг 1.

Создайте папку, которая помечена как доступная **только для чтения** или как **система**.

### <a name="step-2"></a>Шаг 2.

Создайте файл Desktop.ini, содержащий \[ . Шеллклассинфо \] директорикласс = ProgID папки.

### <a name="step-3"></a>Шаг 3.

В реестре создайте **классы hKey \_ с \_ корневой** \\ **папкой ProgID** со значением канусефордиректори. Значение Канусефордиректори позволяет избежать неправильного использования ProgID, которые не участвуют в реализации пользовательских команд для папок с помощью Desktop.ini.

### <a name="step-4"></a>Шаг 4.

Добавьте команды в подключе ProgID **папки** , например:

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a>Примечания

> [!Note]  
> Эти команды могут быть глаголами по умолчанию. в этом случае двойной щелчок папки активирует команду.

 

 

 



