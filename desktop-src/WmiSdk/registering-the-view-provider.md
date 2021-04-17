---
description: Инструментарий WMI автоматически регистрирует библиотеку DLL поставщика представления в процессе установки WMI. Однако для каждого пространства имен, которое будет содержать классы представлений, по-прежнему необходимо зарегистрировать поставщик представления в инструментарии WMI.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Регистрация поставщика представления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530a701d3ffc39523b1b3432dd2d94a3da256605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703180"
---
# <a name="registering-the-view-provider"></a>Регистрация поставщика представления

Инструментарий WMI автоматически регистрирует библиотеку DLL поставщика представления в процессе установки WMI. Однако для каждого пространства имен, которое будет содержать классы представлений, по-прежнему необходимо зарегистрировать поставщик представления в инструментарии WMI.

Следующая процедура описывает, как зарегистрировать поставщик представления.

**Регистрация поставщика представления**

1.  Создайте экземпляр класса [**\_ \_ Win32Provider**](--win32provider.md) для описания реализации поставщика представления.

    Экземпляр [**\_ \_ Win32Provider**](--win32provider.md) описывает имя поставщика и его идентификатор класса (CLSID), а также параметры безопасности по умолчанию.

    В следующем примере кода описывается реализация [**\_ \_ Win32Provider**](--win32provider.md).

    ``` syntax
    instance of __Win32Provider as $DataProv
    {
        Name = "MS_VIEW_INSTANCE_PROVIDER";
        ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
        ImpersonationLevel = 1;
        PerUserInitialization = "True";
        
    };
    ```

2.  Создайте экземпляр класса [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md) .

    В следующем примере кода показано, как создать экземпляр класса **\_ \_ инстанцепровидеррегистратион** .

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $DataProv;
        SupportsPut = True;
        SupportsGet = True;
        SupportsDelete = True;
        SupportsEnumeration = True;
        QuerySupportLevels = {"WQL:UnarySelect"};
    };
    ```

3.  Создайте экземпляр класса [**\_ \_ месодпровидеррегистратион**](--methodproviderregistration.md) , если требуется, чтобы класс представления Union поддерживал методы.

    В следующем примере кода показано, как создать экземпляр класса **\_ \_ месодпровидеррегистратион** .

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  Скомпилируйте MOF-код с помощью компилятора MOF ([mofcomp](mofcomp.md)) или интерфейса [**имофкомпилер**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

    Если вы сохраните приведенный выше пример MOF-кода в файл с именем Виевтест. mof, используйте команду mofcomp, чтобы загрузить MOF-код в целевое пространство имен. *Намеспацепас* — пространство имен, в котором нужно создать экземпляр класса представления.

    Введите следующую команду в командной строке, чтобы загрузить MOF-код в целевое пространство имен.

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    Дополнительные сведения см. в разделе [Компиляция MOF-файлов](compiling-mof-files.md).

Дополнительные сведения см. [в разделе Регистрация поставщика](registering-a-provider.md).

 

 



