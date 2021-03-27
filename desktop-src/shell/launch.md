---
description: После того, как приложение размещает файловый объект, для него часто приходится выполнять следующие действия.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Запуск приложений (ShellExecute, ShellExecuteEx, ШЕЛЛЕКСЕКУТЕИНФО)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e528e6c816040a83d57864999fbb2d683f9fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908744"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a>Запуск приложений (ShellExecute, ShellExecuteEx, ШЕЛЛЕКСЕКУТЕИНФО)

После того, как приложение размещает файловый объект, для него часто приходится выполнять следующие действия. Например, приложению может потребоваться запустить другое приложение, позволяющее пользователю изменять файл данных. Если файл является исполняемым файлом, приложение может захотеть просто запустить его. В этом документе описывается, как использовать [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) или [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) для выполнения этих задач.

-   [Использование ShellExecute и ShellExecuteEx](#using-shellexecute-and-shellexecuteex)
    -   [Команды объекта](#object-verbs)
    -   [Использование ShellExecuteEx для предоставления служб активации с сайта](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [Использование ShellExecute для запуска диалогового окна поиска](#using-shellexecute-to-launch-the-search-dialog-box)
-   [Простой пример использования ShellExecuteEx](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a>Использование ShellExecute и ShellExecuteEx

Чтобы использовать [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) или [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), приложение должно указать объект файла или папки, к которому будет применена операция, и *команду* , указывающую операцию. Для **ShellExecute** присвойте эти значения соответствующим параметрам. Для **ShellExecuteEx** заполните соответствующие элементы структуры [**шеллексекутеинфо**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) . Существует также несколько других элементов или параметров, которые можно использовать для точной настройки поведения двух функций.

Объекты файлов и папок могут быть частью файловой системы или виртуальных объектов, и их можно идентифицировать по путям или указателям на списки идентификаторов элементов (PIDL).

### <a name="object-verbs"></a>Команды объекта

Команды, доступные для объекта, по сути являются элементами, которые находятся в контекстном меню объекта. Чтобы узнать, какие команды доступны, просмотрите реестр в разделе

**HKey \_ \_Корень классов** \\ **CLSID** \\ *{Object \_ CLSID}* \\  \\ *команда* оболочки

где *\_ CLSID объекта* — это идентификатор класса (CLSID) объекта, а *глагол* — имя доступной команды. Подключ  \\ **команды** verb содержит данные, указывающие, что происходит при вызове этой команды.

Чтобы узнать, какие команды доступны для [предопределенных объектов оболочки](handlers.md), просмотрите раздел реестра в разделе

**HKey \_ Классы \_ корневого** \\ *объекта \_ имя* класса \\  \\ *команда* оболочки

где *\_ имя объекта* — это имя предопределенного объекта оболочки. Опять же,  \\ подраздел **команды** verb содержит данные, указывающие, что происходит при вызове этой команды.

Часто доступные команды включают:



| Команда       | Описание                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| изменение;       | Запускает редактор и открывает документ для редактирования.                                                   |
| поиск       | Инициирует поиск, начиная с указанного каталога.                                                |
| open       | Запускает приложение. Если этот файл не является исполняемым файлом, запускается связанное с ним приложение. |
| print      | Выводит файл документа.                                                                                |
| properties | Отображает свойства объекта.                                                                        |
| запуск от имени      | Запускает приложение от имени администратора. Контроль учетных записей (UAC) предложит пользователю подтвердить согласие на |
|            | Запустите приложение с повышенными правами или введите учетные данные администратора, используемого для запуска        |
|            | приложении Aha!.                                                                                             |

 

Каждая команда соответствует команде, которая будет использоваться для запуска приложения из окна консоли. Хорошим примером является команда **Open** , так как она обычно поддерживается. Для файлов exe программа **Open** просто запускает приложение. Однако чаще используется для запуска приложения, которое работает с определенным файлом. Например, файлы. txt могут быть открыты в Microsoft WordPad. Таким образом, команда **Open** для TXT-файла будет соответствовать примерно следующей команде:


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



При использовании [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) или [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) для открытия TXT-файла Wordpad.exe запускается с указанным файлом в качестве аргумента. Некоторые команды могут иметь дополнительные аргументы, например флаги, которые можно добавить при необходимости для правильного запуска приложения. Дальнейшее обсуждение контекстных меню и глаголов см. в разделе [расширение контекстных меню](context.md).

Как правило, попытка определить список доступных команд для определенного файла немного сложна. Во многих случаях можно просто установить для параметра *Лпверб* **значение NULL**, которое вызывает команду по умолчанию для типа файла. Эта процедура обычно эквивалентна установке *лпверб* в значение "Open", но некоторые типы файлов могут иметь разные команды по умолчанию. Дополнительные сведения см. в разделе [расширение контекстных меню](context.md) и справочная документация по [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a>Использование ShellExecuteEx для предоставления служб активации с сайта

Службы цепочки сайтов могут управлять множеством поведений активации элементов. Начиная с Windows 8, можно указать указатель на цепочку сайтов, чтобы [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) для включения этих поведений. Чтобы предоставить сайт **ShellExecuteEx**:

-   Укажите параметр см \_ \_ . флаг маски \_ хинст \_ — \_ флаг сайта в элементе **фмаск** элемента [**шеллексекутеинфо**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).
-   Укажите [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) в члене **хинстапп** объекта [**шеллексекутеинфо**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a>Использование ShellExecute для запуска диалогового окна поиска

Когда пользователь щелкает правой кнопкой мыши значок папки в проводнике Windows, один из пунктов меню — «Search» (Поиск). При выборе этого элемента оболочка запускает свою служебную программу поиска. Эта программа отображает диалоговое окно, которое можно использовать для поиска в файлах указанной текстовой строки. Приложение может программно запустить программу поиска для каталога путем вызова [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)с параметром "Find" в качестве параметра *лпверб* , а путь к каталогу — как параметр *лпфиле* . Например, следующая строка кода запускает программу поиска для каталога c: \\ мипрограмс.


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a>Простой пример использования ShellExecuteEx

В следующем примере консольного приложения показано использование [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa). Для ясности опущена большая часть кода проверки ошибок.


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <objbase.h>

main()
{
    LPITEMIDLIST pidlWinFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfWinFiles = NULL;
    IShellFolder *psfDeskTop = NULL;
    LPENUMIDLIST ppenum = NULL;
    STRRET strDispName;
    TCHAR pszParseName[MAX_PATH];
    ULONG celtFetched;
    SHELLEXECUTEINFO ShExecInfo;
    HRESULT hr;
    BOOL fBitmap = FALSE;

    hr = SHGetFolderLocation(NULL, CSIDL_WINDOWS, NULL, NULL, &pidlWinFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlWinFiles, NULL, IID_IShellFolder, (LPVOID *) &psfWinFiles);
    hr = psfDeskTop->Release();

    hr = psfWinFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfWinFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszParseName, MAX_PATH);
        CoTaskMemFree(pidlItems);
        if(StrCmpI(PathFindExtension(pszParseName), TEXT( ".bmp")) == 0)
        {
            fBitmap = TRUE;
            break;
        }
    }

    ppenum->Release();

    if(fBitmap)
    {
        ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
        ShExecInfo.fMask = NULL;
        ShExecInfo.hwnd = NULL;
        ShExecInfo.lpVerb = NULL;
        ShExecInfo.lpFile = pszParseName;
        ShExecInfo.lpParameters = NULL;
        ShExecInfo.lpDirectory = NULL;
        ShExecInfo.nShow = SW_MAXIMIZE;
        ShExecInfo.hInstApp = NULL;

        ShellExecuteEx(&ShExecInfo);
    }

    CoTaskMemFree(pidlWinFiles);
    psfWinFiles->Release();

    return 0;
}
```



Приложение сначала извлекает ПИДЛ каталога Windows и перечисляет его содержимое до тех пор, пока не найдет первый файл. bmp. В отличие от предыдущего примера, [**ишеллфолдер:: жетдисплайнамеоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) используется для получения имени синтаксического анализа файла вместо его отображаемого имени. Так как это папка файловой системы, имя синтаксического анализа — это полный путь, который необходим для [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

После обнаружения первого BMP-файла соответствующие значения присваиваются элементам структуры [**шеллексекутеинфо**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) . Для элемента **лпфиле** задается имя синтаксического анализа файла, а член **Лпверб** — **значение NULL**, чтобы начать операцию по умолчанию. В этом случае по умолчанию используется операция "Открыть". Структура затем передается в [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), которая запускает обработчик по умолчанию для файлов растрового изображения, обычно MSPaint.exe, чтобы открыть файл. После возврата функции PIDL освобождаются и освобождается интерфейс [**ишеллфолдер**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) папки Windows.

 

 
