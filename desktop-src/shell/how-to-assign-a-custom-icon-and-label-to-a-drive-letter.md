---
description: Укажите пользовательский значок и метку для диска.
ms.assetid: B6EF7F84-7747-4689-B740-A91CA8E394D7
title: Назначить букве диска пользовательский значок и метку
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848c076db443c502a667d67e0b7b49ce51db4ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985476"
---
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a>Как назначить букву диска пользовательский значок и метку

Укажите пользовательский значок и метку для диска.

## <a name="instructions"></a>Инструкции

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a>Шаг 1. Замена стандартного значка диска на пользовательский значок в Windows 2000

Чтобы заменить стандартный значок диска на пользовательский значок в Windows 2000, добавьте подраздел с именем для буквы диска в следующий раздел.

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

В следующем примере задается пользовательский значок и метка для диска E:. Значок находится в файле C: \\ MyDir \\MyDrive.exe с нулевым индексом, начинающимся с нуля.

Для Windows 2000:

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
            E
               DefaultIcon
                  (Default) = C:\MyDir\MyDrive.exe,3
               DefaultLabel
                  (Default) = MyDrive
```

### <a name="step-2-replacing-the-standard-drive-icon-with-a-custom-icon-in-all-other-versions-of-windows"></a>Шаг 2. Замена стандартного значка диска на пользовательский значок во всех остальных версиях Windows

Чтобы заменить стандартный значок диска на пользовательский значок во всех версиях Windows, отличных от Windows 2000, добавьте подраздел с именем для буквы диска в следующий раздел.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
```

В следующем примере задается пользовательский значок и метка для диска E:. Значок находится в файле C: \\ MyDir \\MyDrive.exe с нулевым индексом, начинающимся с нуля.

Для всех остальных версий Windows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
                     E
                        DefaultIcon
                           (Default) = C:\MyDir\MyDrive.exe,3
                        DefaultLabel
                           (Default) = MyDrive
```

### <a name="step-3-calling-the-shupdateimage-event"></a>Шаг 3. вызов события Шупдатеимаже

Во всех версиях Windows при изменении типа файла или значка диска необходимо также вызвать Шупдатеимаже, чтобы уведомить оболочку о необходимости обновления значков, отображаемых в данный момент.

## <a name="remarks"></a>Примечания

За буквой диска не следует ставить двоеточие (:). Добавьте подраздел **дефаултикон** в подраздел букв диска и задайте в качестве значения по умолчанию строку, содержащую расположение значка. Первая часть строки содержит полный путь к файлу значка. Если в файле содержится более одного значка, за ним следует запятая, а затем — Отсчитываемый от нуля индекс значка.

 

 



