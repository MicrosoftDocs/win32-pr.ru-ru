---
description: Приложения, процессы и Windows могут сделать недоступными для закрепления на панели задач или для включения в список наиболее часто используемых программных решений в меню "Пуск".
title: Как исключить элементы из закрепления панели задач и последних или часто встречающихся списков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f32ad641832703804f94b8cc28f47ea9cabb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985441"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a>Как исключить элементы из закрепления панели задач и последних или часто встречающихся списков

Приложения, процессы и Windows могут сделать недоступными для закрепления на панели задач или для включения в список наиболее часто используемых программных решений в меню " **Пуск** ".

## <a name="instructions"></a>Инструкции


Существует три механизма для выполнения исключения элементов из списка закрепления панели задач и последних или часто встречающихся списков.

-   Добавьте запись OnStartPage в регистрацию приложения, как показано в следующем примере:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    Данные, связанные с записью "OnStartPage", игнорируются. Требуется только присутствие записи. Таким образом, идеальный тип для OnStartPage — **reg \_ None**.

    Обратите внимание, что любое использование явного идентификатора модели пользователя приложения (AppUserModelID) переопределяет запись OnStartPage. Если явный AppUserModelID применяется к ярлыку, процессу или окну, он становится также прикрепляемые и доступен для списка наиболее часто используемых в меню " **Пуск** ".

-   Задайте свойство [System. аппусермодел. превентпиннинг](../properties/props-system-appusermodel-preventpinning.md) в окнах и сочетаниях клавиш. Это свойство должно быть установлено в окне до установки свойства [ \_ аппусермодел \_ ID для PKEY](../properties/props-system-appusermodel-id.md) .
-   Добавьте явный AppUserModelID в качестве значения в следующий подраздел реестра, как показано в следующем примере:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    Каждая запись является значением **reg \_ null** с именем AppUserModelID. Любой AppUserModelID, найденный в этом списке, не также прикрепляемые и не может быть включен в список часто используемых меню " **Пуск** ".

## <a name="remarks"></a>Примечания

Имейте в виду, что определенные исполняемые файлы, а также ярлыки, содержащие определенные строки в своих именах, автоматически исключаются из закрепления и включения в список часто используемых программ.

> [!Note]  
> Это автоматическое исключение можно переопределить, применив явный AppUserModelID.

 

Если любая из следующих строк, независимо от регистра, включается в имя ярлыка, программа не также прикрепляемые и не отображается в списке наиболее часто используемых (неприменимо к Windows 10):

-   Документация
-   Справка
-   Установка
-   Подробнее
-   Чтение
-   Сначала прочитать
-   Readme
-   Удалить
-   Настройка
-   Поддержка
-   What's New

Следующий список программ не также прикрепляемые и исключен из списка наиболее часто используемых:

-   Applaunch.exe
-   Control.exe
-   Dfsvc.exe
-   Dllhost.exe
-   Guestmodemsg.exe
-   Hh.exe
-   Install.exe
-   Isuninst.exe
-   Lnkstub.exe
-   Mmc.exe
-   Mshta.exe
-   Msiexec.exe
-   Msoobe.exe
-   Rundll32.exe
-   Setup.exe
-   St5unst.exe
-   Unwise.exe
-   Unwise32.exe
-   Werfault.exe
-   Winhlp32.exe
-   Wlrmdr.exe
-   Wuapp.exe

Приведенные выше списки хранятся в следующих значениях реестра.

> [!Note]  
> Эти списки не должны изменяться приложениями. Используйте один из методов списка исключений, описанных ранее в этом разделе, для того же интерфейса.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[Панель задач](taskbar.md)
</dt> <dt>

[Расширения панели задач](taskbar-extensions.md)
</dt> </dl>

 

 
