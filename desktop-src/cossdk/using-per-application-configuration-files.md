---
description: Использование файлов конфигурации Per-Application
ms.assetid: a600e5a4-b2bb-45a6-8b86-5ea3caf7aa78
title: Использование файлов конфигурации Per-Application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bbc38a2433d2da6d2a39985523a5ebffd0d971102bc883e44ae24d9fcc165ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372344"
---
# <a name="using-per-application-configuration-files"></a>Использование файлов конфигурации Per-Application

Для использования файлов конфигурации COM+ для каждого приложения необходимо выполнить следующие основные действия.

-   Настройка корневого каталога приложения для приложения COM+.
-   Создайте файлы Application. manifest и application.config в корневом каталоге приложения COM+.

> [!Note]  
> файлы конфигурации для каждого приложения доступны только начиная с Windows XP с пакетом обновления 2 (sp2) и Windows Server 2003.

 

**Использование файла конфигурации для каждого приложения**

1.  Создайте библиотеку классов .NET со ссылкой на сборку System. EnterpriseServices.

2.  Библиотека классов должна содержать следующий код:

    ```CSharp
    using System;
    using System.Configuration;
    using System.EnterpriseServices;

    public class Class1 : ServicedComponent
    {
        public string GetConfigData()
        {
            return System.Configuration.ConfigurationSettings.AppSettings
                 ["ConfigData1"];
        }
    }
    ```

    

    Обратите внимание, что "ConfigData1" — это пример имени параметра. Его можно заменить именем выбранного параметра.

3.  Создайте пустое приложение COM+. Инструкции по выполнению этой задачи см. в разделе [Создание нового приложения COM+](creating-a-new-com--application.md).
4.  Установите библиотеку классов, созданную в приложении COM+. Инструкции по выполнению этой задачи см. в разделе [Установка новых компонентов](installing-new-components.md).
5.  В средстве администрирования "службы компонентов" щелкните правой кнопкой мыши созданное приложение COM+ и выберите пункт **Свойства**.
6.  В диалоговом окне **Свойства** перейдите на вкладку **Активация** .
7.  Убедитесь, что для параметра **тип активации** задано значение **серверное приложение**.
8.  В текстовом поле **корневой каталог приложения** введите путь или перейдите к каталогу, в котором вы хотите сохранить файлы конфигурации приложения для этого приложения.
9.  Нажмите кнопку **ОК**.

    Обратите внимание, что корневой каталог приложения COM+ можно также указать с помощью свойства Аппликатиондиректори класса [**комадминкаталогобжект**](comadmincatalogobject.md) . Дополнительные сведения см. в разделе [**приложения**](applications.md).

10. В каталоге, выбранном для хранения файлов конфигурации приложения, создайте файл с именем *Application*. manifest. В текстовом редакторе добавьте в этот файл следующий текст:

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" />
    ```

11. В том же каталоге создайте файл с именем *application*.config. В текстовом редакторе добавьте в этот файл следующий текст:

    ``` syntax
    <?xml version="1.0"?>
    <configuration>
        <appSettings>
            <add key="ConfigData1" value="Configuration Data Number 1"/>
        </appSettings>
    </configuration>
    ```

    Обратите внимание, что этот файл конфигурации является всего лишь примером. Можно создать несколько ключей с разными именами и значениями. Однако обратите внимание, что "ConfigData1" соответствует имени параметра, используемого в библиотеке классов, созданной ранее.

12. Создайте консольное приложение .NET со ссылкой на созданную ранее библиотеку классов .NET и ссылку на сборку System. EnterpriseServices.
13. Консольное приложение должно содержать следующий код:
    ```CSharp
    using System;
    using System.IO;

    class Client
    {
    [STAThread]
        static void Main(string[] args)
        {
            Class1 server = new Class1();
            Console.WriteLine(server.GetConfigData());
            Console.ReadLine();
        }
    }
    ```

    

Запустите консольное приложение. Результат должен выглядеть примерно так:

``` syntax
Configuration Data Number 1
```

 

 



