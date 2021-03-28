---
description: API оболочки предоставляет функции, которые можно использовать для управления сетевыми принтерами. Если с файлом связана команда печати, для ее печати можно использовать команду ShellExecuteEx.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Управление принтерами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e9625fbe17c0dd350a10c0c71dcd5332fb9154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985637"
---
# <a name="managing-printers"></a>Управление принтерами

API оболочки предоставляет функции, которые можно использовать для управления сетевыми принтерами. Если с файлом связана команда **печати** , для ее печати можно использовать команду [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .

-   [Управление принтерами](#printer-management)
-   [Печать файлов с помощью ShellExecuteEx](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a>Управление принтерами

Вы можете управлять принтерами в системе с помощью функции [**шинвокепринтеркомманд**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) . Эта функция позволяет выполнять следующие задачи:

-   Установка принтеров.
-   Откройте принтеры.
-   Получение свойств принтера.
-   Создание ссылок на принтеры.
-   Напечатайте тестовую страницу.

## <a name="printing-files-with-shellexecuteex"></a>Печать файлов с помощью ShellExecuteEx

Если с типом файла связана команда печати, можно напечатать файл, вызвав [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) с параметром **Print** в качестве команды. Эта команда часто совпадает с той, которая используется для команды **Open** , с добавлением флага, указывающего приложению распечатать файл. Например, файлы. txt могут быть распечатаны с помощью Microsoft WordPad. Таким образом, команда **Open** для TXT-файла будет соответствовать примерно следующей команде:


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



При использовании [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) для печати TXT-файла WordPad открывает файл, выводит его на печать, а затем закрывает, возвращая управление приложению. Следующий пример функции принимает полный путь и использует **ShellExecuteEx** для печати, используя команду Print, связанную с расширением имени файла.


```C++
#include <shlobj.h>

HINSTANCE PrintFile(LPCTSTR pszFileName)
{
    SHELLEXECUTEINFO ShExecInfo;
    HINSTANCE hInst;

    // Fill the SHELLEXECUTEINFO array.

    ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
    ShExecInfo.fMask = NULL;
    ShExecInfo.hwnd = NULL;
    ShExecInfo.lpVerb = "print";
    ShExecInfo.lpFile = pszFileName;  // a fully qualified path
    ShExecInfo.lpParameters = NULL;
    ShExecInfo.lpDirectory = NULL;    
    ShExecInfo.nShow = SW_MAXIMIZE;
    ShExecInfo.hInstApp = NULL;

    hInst = ShellExecuteEx(&ShExecInfo);
    
    return hInst;
}
```



 

 



