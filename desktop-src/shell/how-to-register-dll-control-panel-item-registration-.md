---
description: Элементы панели управления, реализованные в библиотеке DLL, которая экспортирует функцию Кплапплет, имеют разные требования к регистрации, чем .exe файлов.
title: Регистрация элементов панели управления DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25fffb3b06f93640c5ca8623fb24ffb53c6fd3ecae0b9e23cabafacdceba8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593194"
---
# <a name="how-to-register-dll-control-panel-items"></a>Регистрация элементов панели управления DLL

> [!Note]  
> Текущие рекомендации по реализации состояния, когда новые элементы панели управления должны быть реализованы как .exe файлы, а не .cpl файлы. Приведенная ниже информация включается в основном для устаревших целей.

 

Элементы панели управления, реализованные в библиотеке DLL, которая экспортирует функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) , имеют разные требования к регистрации, чем .exe файлов. начиная с Windows XP новые библиотеки элементов панели управления должны быть установлены в папку соответствующего приложения в папке Program files. Элементы, хранящиеся в каталоге System32 с расширением .cpl, не обязательно регистрировать. они автоматически отображаются на панели управления. Все остальные элементы панели управления, использующие **кплапплет** , должны быть зарегистрированы одним из двух способов:

-   если элемент панели управления должен быть доступен всем пользователям, зарегистрируйте путь для каждого компьютера, добавив параметр **REG \_ EXPAND \_ SZ** в раздел **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **панели управления** \\ **Cpls** , указав путь к библиотеке DLL.
-   Если элемент панели управления должен быть доступен отдельно для каждого пользователя, используйте раздел **hKey \_ текущий \_ пользователь** в качестве корневого ключа вместо **\_ локального \_ компьютера hKey**.

В следующих двух примерах регистрируется элемент панели управления *микплапп* . Библиотека DLL называется MyCpl.cpl и находится в каталоге приложения *MyCorp \\ MyApp* . В первом примере демонстрируется регистрация на компьютере.

## <a name="instructions"></a>Инструкции

### <a name="step-1"></a>Шаг 1.

Добавьте эти сведения в реестр для регистрации существования файла .cpl.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Cpls
                     MyCpl = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl
```

### <a name="step-2"></a>Шаг 2.

**Windows Vista и более поздних версий:** Добавьте эти дополнительные сведения в реестр, чтобы предоставить идентификатор GUID для элемента панели управления.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.AppId
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = {A newly generated GUID}
```

Создавая идентификатор GUID для уникальной идентификации элемента панели управления, можно добавить ссылки задач в панель управления. Без этого GUID ссылки на задачи не будут связаны с элементом панели управления. См. раздел [Создание ссылок на задачи с возможностью поиска для элемента панели управления](creating-searchable-task-links.md).

### <a name="step-3"></a>Шаг 3.

**Windows Vista и более поздних версий:** Добавьте следующие сведения в реестр, чтобы создать каноническое имя для элемента.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ApplicationName
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] MyCorporation.MyCpl
```

Добавляя каноническое имя, пользователи могут запускать элемент панели управления из командной строки, вводя `control.exe /name MyCorporation.MyCpl` . Это также позволяет изменять реализацию из файла .cpl в файл .exe, не требуя от них внесения каких-либо изменений, так как они могут продолжать открывать элемент по его каноническому имени. Дополнительные сведения об канонических именах см. в разделе [исполнение элементов панели управления](executing-control-panel-items.md).

### <a name="step-4"></a>Шаг 4.

**Windows Vista и более поздних версий:** Добавьте следующие сведения в реестр, чтобы назначить элемент панели управления одной или нескольким категориям.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.Category
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

**Windows XP:** Добавьте следующие сведения в реестр, чтобы назначить элемент панели управления одной или нескольким категориям.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     {305CA226-D286-468e-B848-2B2E8E697B74} 2
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

В этом примере элемент назначается категории 3, которая является сетью и Интернетом. Чтобы добавить элемент в несколько категорий, укажите в качестве \_ значения reg SZ значение, разделенное запятыми, например "3, 8". Значения могут быть указаны в виде десятичного или шестнадцатеричного числа. обратите внимание, что возможность добавления элемента к нескольким категориям возможна только в Windows XP с пакетом обновления 2 (sp2) и более поздних версиях. См. раздел [Назначение категорий панели управления](assigning-control-panel-categories.md) для всех возможных значений.

### <a name="step-5"></a>Шаг 5.

**Windows Vista и более поздних версий:** Добавьте следующие сведения в реестр для создания и наведите указатель на XML-файл, содержащий ссылки на задачи для данного элемента. Значение должно представлять собой \_ путь к reg-SZ, как показано здесь, а также модуль и идентификатор ресурса (например, "C: \\ Program Files \\ MyCorp \\ MyApp \\MyApp.exe,-31"), если это внедренный ресурс. Расположение XML-файла должно быть указано полностью. Он не может использовать переменную среды, например% ProgramFiles%.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.TasksFileUrl
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] C:\ProgramFiles\MyCorp\MyApp\MyTasks.xml
```

Дополнительные сведения о связях задач и о создании XML-файла для их хранения см. [в разделе Создание ссылок на задачи с возможностью поиска для элемента панели управления](creating-searchable-task-links.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Регистрация элементов панели управления](registering-control-panel-items.md)
</dt> <dt>

[Регистрация исполняемых элементов панели управления](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
