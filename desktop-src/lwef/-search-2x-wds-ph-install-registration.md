---
title: установка и регистрация обработчиков протоколов (устаревшие функции Windows среды)
description: Установка обработчиков протоколов включает копирование библиотек DLL в соответствующее расположение в каталоге Program Files и их регистрацию.
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f6cce4337c8b2c3faf47411f76165b11ed13ff00dfebd66ac5307d6ca6a68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716564"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a>установка и регистрация обработчиков протоколов (устаревшие функции Windows среды)

> [!NOTE]
> Windows настольный поиск 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003. в более поздних выпусках используйте вместо этого [Windows поиск](../search/-search-3x-wds-overview.md) .

Установка **обработчиков протоколов** включает копирование библиотек DLL в соответствующее расположение в каталоге Program Files и их регистрацию.

В этом разделе рассматриваются следующие вопросы.

-   [Рекомендации по установке](#installation-guidelines)
-   [Регистрация обработчиков протоколов](#to-register-protocol-handlers)
-   [Регистрация расширений оболочки](#to-register-shell-extensions)

## <a name="installation-guidelines"></a>Рекомендации по установке

Обработчики протоколов должны реализовать самостоятельную регистрацию для установки и следовать приведенным ниже рекомендациям.

-   Установщик должен использовать установщик EXE или MSI.
-   Необходимо указать заметки о выпуске.
-   Для каждой установленной надстройки необходимо создать запись « **Установка и удаление программ** ».
-   Установщик должен задействовать все параметры реестра для конкретного типа файлов или хранить данные, распознаваемые текущей надстройкой.
-   Если предыдущая надстройка перезаписывается, установщик должен уведомить пользователя.
-   Если более новая надстройка перезаписала предыдущую надстройку, то должна быть возможность восстановить функциональность предыдущей надстройки и сделать ее надстройкой по умолчанию для этого типа файлов.

## <a name="to-register-protocol-handlers"></a>Регистрация обработчиков протоколов

Для регистрации компонента обработчика протокола необходимо внести в реестр записи четырнадцать, где:

-   *Версия \_ Параметр \_* "DIB ProgID" — это независимый от версии идентификатор ProgID реализации обработчика протокола
-   *Версия \_ DEP \_ ProgID* — это зависимый от версии идентификатор ProgID реализации обработчика протокола.
-   *CLSID \_ 1* — это CLSID реализации обработчика протокола

1.  Зарегистрируйте независимый от версии идентификатор ProgID со следующими ключами и значениями:

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CurVer
       (Default) = <Ver_Dep_ProgID>
    ```

2.  Зарегистрируйте версию ProgID, зависимую от версии, со следующими ключами и значениями:

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  Зарегистрируйте CLSID обработчика протокола со следующими ключами и значениями:

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/InprocServer32
       (Default) = <DLL Install Path>
       Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ProgID
       (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ShellFolder
       Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/TypeLib
       (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/VersionIndependentProgID
       (Default) = <Ver_Ind_ProgID>"
    ```

4.  регистрация обработчика протокола с помощью Windows Desktop Search:

    ```
    HKEY_LOCAL_MACHINE\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\Windows Desktop Search\DS\Index\ProtocolHandlers\<Protocol Name>
       HasRequirements = dword:00000000
       HasStartPage = dword:00000000
    ```

## <a name="to-register-shell-extensions"></a>Регистрация расширений оболочки

Чтобы зарегистрировать расширение оболочки обработчика протокола, необходимо создать две записи в реестре.

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




