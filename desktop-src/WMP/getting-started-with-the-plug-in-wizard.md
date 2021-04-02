---
title: начало работы с помощью мастера подключаемых модулей
description: начало работы с помощью мастера подключаемых модулей
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Подключаемые модули проигрывателя Windows Media, Установка подключаемого модуля
- подключаемые модули, Установка подключаемого модуля
- Создание подключаемых модулей, мастер установки подключаемых модулей
- Мастер подключаемых модулей проигрывателя Windows Media, установка
- Мастер установки подключаемых модулей
- Мастер подключаемых модулей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4feb9cfa60c120bfc5bb675ea8a8078b95ad14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986684"
---
# <a name="getting-started-with-the-plug-in-wizard"></a>начало работы с помощью мастера подключаемых модулей

Чтобы настроить среду разработки для создания подключаемых модулей проигрывателя Windows Media, необходимо установить следующие компоненты:

-   Microsoft Visual Studio .NET 2003 или более поздней версии
-   Проигрыватель Windows Media 9 Series или более поздней версии
-   Windows SDK, который включает в себя пакет SDK для проигрывателя Windows Media
-   Мастер подключаемых модулей проигрывателя Windows Media

## <a name="installing-the-wizard"></a>Установка мастера

Чтобы установить мастер подключаемых модулей проигрывателя Windows Media, выполните следующие действия.

1.  Откройте папку, в которую вы установили Windows SDK. Разверните папку, чтобы просмотреть ее вложенные папки, и перейдите к примерам \\ \\ \\ мастеров мультимедиа WMP \\ вмпвиз.
2.  Нахождение следующих трех файлов:
    -   вмпвиз. vsz
    -   вмпвиз. VSDir
    -   вмпвиз. ico
3.  С помощью текстового редактора, например Блокнота, измените файл вмпвиз. vsz.

    Найдите следующую строку:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Измените `<VsWizardEngine version goes here>` одно из следующих значений в зависимости от установленной версии Visual Studio.

    

    | Значение              | Версия Visual Studio   |
    |--------------------|-------------------------|
    | Всвизарденгине. 7.1 | Visual Studio .NET 2003 |
    | Всвизарденгине. 8.0 | Visual Studio 2005      |
    | Всвизарденгине. 9.0 | Visual Studio 2008      |

    

     

    Найдите следующую строку:

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    Перейдите `<path to wmpwiz directory goes here>` к пути, где расположены файлы мастера.

    Например, предположим, что у вас есть Visual Studio 2008, а файлы мастера находятся здесь: C: \\ Program Files \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ \\ Media WMP \\ Wizards \\ вмпвиз. Затем файл вмпвиз. vsz будет выглядеть следующим образом:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Откройте папку, в которой установлена Visual Studio. Разверните папку, чтобы просмотреть ее вложенные папки, и выберите папку с именем вкпрожектс.
5.  Скопируйте три файла, перечисленные в шаге 2, в папку вкпрожектс. Теперь мастер установлен.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание подключаемого модуля](building-a-plug-in.md)
</dt> <dt>

[Использование мастера подключаемых модулей в Visual Studio](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




