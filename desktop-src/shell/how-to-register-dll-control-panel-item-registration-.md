---
description: Элементы панели управления, реализованные в библиотеке DLL, которая экспортирует функцию Кплапплет, имеют различные требования к регистрации, чем exe-файлы.
title: Регистрация элементов панели управления DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b82225dcb40487c60210752b2c15af23f95bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813697"
---
# <a name="how-to-register-dll-control-panel-items"></a>Регистрация элементов панели управления DLL

> [!Note]  
> Текущие рекомендации по реализации содержат новые элементы панели управления, которые должны быть реализованы в виде exe, а не файлов. cpl. Приведенная ниже информация включается в основном для устаревших целей.

 

Элементы панели управления, реализованные в библиотеке DLL, которая экспортирует функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) , имеют различные требования к регистрации, чем exe-файлы. Начиная с Windows XP, новые библиотеки элементов панели управления должны быть установлены в папку соответствующего приложения в папке Program Files. Не обязательно регистрировать элементы, хранящиеся в каталоге System32 с расширением. cpl; они автоматически отображаются на панели управления. Все остальные элементы панели управления, использующие **кплапплет** , должны быть зарегистрированы одним из двух способов:

-   Если элемент панели управления должен быть доступен всем пользователям, зарегистрируйте путь для каждого компьютера, добавив параметр **reg \_ expand \_ SZ** в раздел **hKey \_ Local \_ Machine** \\ **Software** \\  \\  \\  \\ **панели управления** Microsoft Windows CurrentVersion \\ **CPLS** , указав путь к библиотеке DLL.
-   Если элемент панели управления должен быть доступен отдельно для каждого пользователя, используйте раздел **hKey \_ текущий \_ пользователь** в качестве корневого ключа вместо **\_ локального \_ компьютера hKey**.

В следующих двух примерах регистрируется элемент панели управления *микплапп* . Библиотека DLL называется MyCpl.cpl и находится в каталоге приложения *MyCorp \\ MyApp* . В первом примере демонстрируется регистрация на компьютере.

## <a name="instructions"></a>Инструкции

### <a name="step-1"></a>Шаг 1.

Добавьте эти сведения в реестр для регистрации существования файла. cpl.

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

**Windows Vista и более поздние версии:** Добавьте эти дополнительные сведения в реестр, чтобы предоставить идентификатор GUID для элемента панели управления.

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

**Windows Vista и более поздние версии:** Добавьте следующие сведения в реестр, чтобы создать каноническое имя для элемента.

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

Добавляя каноническое имя, пользователи могут запускать элемент панели управления из командной строки, вводя `control.exe /name MyCorporation.MyCpl` . Это также позволяет изменить реализацию из CPL-файла на exe-файл, не требуя от программы вызывать какие-либо изменения, так как они могут продолжить открытие элемента по его каноническому имени. Дополнительные сведения об канонических именах см. в разделе [исполнение элементов панели управления](executing-control-panel-items.md).

### <a name="step-4"></a>Шаг 4.

**Windows Vista и более поздние версии:** Добавьте следующие сведения в реестр, чтобы назначить элемент панели управления одной или нескольким категориям.

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

В этом примере элемент назначается категории 3, которая является сетью и Интернетом. Чтобы добавить элемент в несколько категорий, укажите в качестве \_ значения reg SZ значение, разделенное запятыми, например "3, 8". Значения могут быть указаны в виде десятичного или шестнадцатеричного числа. Обратите внимание, что возможность добавления элемента в несколько категорий возможна только в Windows XP с пакетом обновления 2 (SP2) и более поздних версий. См. раздел [Назначение категорий панели управления](assigning-control-panel-categories.md) для всех возможных значений.

### <a name="step-5"></a>Шаг 5.

**Windows Vista и более поздние версии:** Добавьте следующие сведения в реестр для создания и наведите указатель на XML-файл, содержащий ссылки на задачи для данного элемента. Значение должно представлять собой \_ путь к reg-SZ, как показано здесь, а также модуль и идентификатор ресурса (например, "C: \\ Program Files \\ MyCorp \\ MyApp \\MyApp.exe,-31"), если это внедренный ресурс. Расположение XML-файла должно быть указано полностью. Он не может использовать переменную среды, например% ProgramFiles%.

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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Регистрация элементов панели управления](registering-control-panel-items.md)
</dt> <dt>

[Регистрация исполняемых элементов панели управления](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
