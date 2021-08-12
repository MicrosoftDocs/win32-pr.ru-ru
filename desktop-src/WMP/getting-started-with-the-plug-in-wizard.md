---
title: начало работы с помощью мастера подключаемых модулей
description: начало работы с помощью мастера подключаемых модулей
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- подключаемые модули проигрыватель Windows Media, установка подключаемого модуля
- подключаемые модули, Установка подключаемого модуля
- Создание подключаемых модулей, мастер установки подключаемых модулей
- проигрыватель Windows Media Мастер подключаемых модулей, установка
- Мастер установки подключаемых модулей
- Мастер подключаемых модулей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2699d0316be93f6387bdc64c6671df868eaa70fb24a4ad3619026524106432
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576583"
---
# <a name="getting-started-with-the-plug-in-wizard"></a>начало работы с помощью мастера подключаемых модулей

чтобы настроить среду разработки для создания подключаемых модулей проигрыватель Windows Media, необходимо установить следующие компоненты:

-   Microsoft Visual Studio .net 2003 или более поздней версии
-   проигрыватель Windows Media 9 Series или более поздней версии
-   Windows пакет sdk, включающий пакет sdk для проигрыватель Windows Media
-   проигрыватель Windows Media Мастер подключаемых модулей

## <a name="installing-the-wizard"></a>Установка мастера

чтобы установить мастер подключаемых модулей проигрыватель Windows Media, выполните следующие действия.

1.  откройте папку, в которую вы установили Windows SDK. Разверните папку, чтобы просмотреть ее вложенные папки, и перейдите к примерам \\ \\ \\ мастеров мультимедиа WMP \\ вмпвиз.
2.  Нахождение следующих трех файлов:
    -   вмпвиз. vsz
    -   вмпвиз. VSDir
    -   вмпвиз. ico
3.  с помощью текстового редактора, например Блокнот, измените файл вмпвиз. vsz.

    Найдите следующую строку:

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    измените `<VsWizardEngine version goes here>` одно из следующих значений в зависимости от установленной версии Visual Studio.

    

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

    например, предположим, что имеется Visual Studio 2008, а файлы мастера находятся здесь: C: \\ Program files \\ Microsoft sdks \\ Windows \\ v 7.0 \\ samples \\ \\ \\ вмпвиз мастера мультимедиа WMP \\ . Затем файл вмпвиз. vsz будет выглядеть следующим образом:

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Откройте папку, в которую вы установили Visual Studio. Разверните папку, чтобы просмотреть ее вложенные папки, и выберите папку с именем вкпрожектс.
5.  Скопируйте три файла, перечисленные в шаге 2, в папку вкпрожектс. Теперь мастер установлен.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание подключаемого модуля](building-a-plug-in.md)
</dt> <dt>

[Использование мастера подключаемых модулей с Visual Studio](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




