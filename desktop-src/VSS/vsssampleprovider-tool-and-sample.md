---
description: Показывает, как использовать интерфейсы VSS для создания поставщика оборудования VSS.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Средство Всссамплепровидер и пример
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fceaa65b851e5469a3e82323da92d8bde0651a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692350"
---
# <a name="vsssampleprovider-tool-and-sample"></a>Средство Всссамплепровидер и пример

Показывает, как использовать [интерфейсы](volume-shadow-copy-api-interfaces.md) VSS для создания поставщика оборудования VSS.

> [!Note]  
> Средство Всссамплепровидер и пример включены в пакет средств разработки программного обеспечения Microsoft Windows (SDK). Вы можете скачать Windows SDK из [пакета средств разработки программного обеспечения (SDK) для Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).

 

В Windows SDK установки средство Всссамплепровидер можно найти в `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (для 64-разрядной версии Windows) и `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (для 32-разрядной версии Windows).

> [!Note]  
> Поставщики оборудования поддерживаются только в операционных системах Windows Server. В клиентской операционной системе Windows можно скомпилировать пример Всссамплепровидер, но нельзя зарегистрировать его в качестве поставщика оборудования.

 

Средство Всссамплепровидер состоит из следующих файлов:

-   Virtualstorage.sys
-   Vstorcontrol.exe
-   Vssampleprovider.dll
-   Vstorinterface.dll

Пример Всссамплепровидер включает следующие скрипты установки и удаления:

-   Инсталл-самплепровидер. cmd
-   Унинсталл-самплепровидер. cmd
-   Регистрация \_app.vbs

**Установка и использование образца Всссамплепровидер**

1.  Перейдите к каталогу `Program Files (x86)\Windows Kits\8.0\bin\`. Этот каталог содержит virtualstoragevss.sys и vstorcontrol.exe.
2.  Откройте окно командной строки в указанном каталоге.
3.  Чтобы установить драйвер виртуального хранилища, в окне командной строки введите следующую команду:

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  Чтобы установить пример поставщика VSS, в окне командной строки введите следующую команду:

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  Чтобы создать виртуальный LUN, выполните следующие действия.

    1.  В окне командной строки введите следующую команду:

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        Эта команда создает виртуальный LUN, идентификатор хранения которого является **примером поставщика оборудования VSS**. Чтобы создать дополнительные виртуальные LUN, повторите этот шаг.

        Пример поставщика VSS распознает LUN только в том случае, если **образец VSS поставщика оборудования** является частью идентификатора хранилища. Дополнительные сведения об идентификаторе хранилища см. в следующей записи блога.

        [LUN. Повторная синхронизация с Diskshadow и виртуальным хранилищем](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  В окне командной строки используйте diskpart.exe, чтобы отформатировать виртуальный диск и назначить ему букву диска.

        Ниже приведен пример сценария для выполнения в командной строке DiskPart.

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  Чтобы запустить пример поставщика, в окне командной строки введите следующую команду:

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    *<drive>* представляет букву диска виртуального LUN.

7.  Чтобы удалить пример поставщика VSS, в окне командной строки введите следующую команду:

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  Чтобы удалить драйвер виртуального хранилища, в окне командной строки введите следующую команду:

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



