---
description: Поставщик системного реестра регистрируется как часть процесса установки WMI в Windows.
ms.assetid: ce5d0785-6e1b-411c-91df-f25767310530
ms.tgt_platform: multiple
title: Регистрация поставщика системного реестра
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d600872c4efab5560f4fd794cac63beb4365841c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702003"
---
# <a name="registering-the-system-registry-provider"></a>Регистрация поставщика системного реестра

Поставщик системного реестра регистрируется как часть процесса установки WMI в Windows. Если вы используете другую платформу и хотите использовать поставщик системного реестра, необходимо сначала зарегистрировать поставщик, выполнив описанные ниже действия.

В следующей процедуре описывается регистрация поставщика системного реестра.

**Регистрация поставщика системного реестра**

1.  Зарегистрируйте поставщик в качестве сервера COM.

    При необходимости может потребоваться создать записи реестра. Этот процесс применяется ко всем COM-серверам и не связан с WMI. Дополнительные сведения см. в документации по [com](https://msdn.microsoft.com/library/aa139695.aspx) в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows.

2.  Создайте экземпляр класса [**\_ \_ Win32Provider**](--win32provider.md) для описания реализации поставщика системного реестра.

    Экземпляр [**\_ \_ Win32Provider**](--win32provider.md) описывает имя поставщика и его идентификатор класса (**CLSID**).

    В следующем примере показано, как зарегистрировать [**\_ \_ Win32Provider**](--win32provider.md) в качестве свойства экземпляра, события или поставщика метода.

    ``` syntax
    // Instance provider
    instance of __Win32Provider as $InstProv
    {
        Name    = "RegProv" ;
        ClsId   = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}" ;
    };    
    // Property provider 
    instance of __Win32Provider as $PropProv 
    {
        Name = "RegPropProv"; 
        Clsid = "{72967901-68EC-11d0-B729-00AA0062CBB7}"; 
    }; 
    // Event provider
    instance of __Win32Provider as $RegEvent
    {
        Name = "RegistryEventProvider";
        Clsid = "{fa77a74e-e109-11d0-ad6e-00c04fd8fdff}";
    };
    instance of __Win32Provider as $RegMethod
    {
        Name = "RegistryMethodProvider";
        Clsid = "{44DE513E-60C2-11d3-AF33-00C04F79FEB1}";
    };
    ```

3.  Создайте один или несколько экземпляров классов, производных от класса [**\_ \_ провидеррегистратион**](--providerregistration.md) , чтобы описать логическую реализацию поставщика системного реестра.

    В зависимости от цели регистрации поставщика системного реестра можно создать один или несколько следующих классов.

    [**\_\_инстанцепровидеррегистратион**](--instanceproviderregistration.md)

    [**\_\_пропертипровидеррегистратион**](--propertyproviderregistration.md)

    [**\_\_евентпровидеррегистратион**](--eventproviderregistration.md)

    [**\_\_месодпровидеррегистратион**](--methodproviderregistration.md)

    В следующем примере кода MOF описывается, как можно зарегистрировать поставщик системного реестра в качестве экземпляра, свойства, события или поставщика метода.

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $InstProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
        SupportsDelete = FALSE;
        SupportsEnumeration = TRUE;
    };
    instance of __PropertyProviderRegistration
    {
        Provider = $PropProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
    }; 
    instance of __EventProviderRegistration
    {
        Provider = $RegEvent;
        EventQueryList = {
                "select * from RegistryKeyChangeEvent",
                "select * from RegistryValueChangeEvent",
                "select * from RegistryTreeChangeEvent"};
    };
    // Method provider
    instance of __MethodProviderRegistration
    {
        Provider = $RegMethod;
    };
    ```

4.  Скомпилируйте MOF-файл с помощью компилятора MOF или интерфейса [**имофкомпилер**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

Файл режевент. mof, указанный в разделе WMI Windows SDK, содержит экземпляры [**\_ \_ Win32Provider**](--win32provider.md) и [**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md) , необходимые для регистрации поставщика системных реестров в качестве поставщика событий. Дополнительные сведения о регистрации поставщика см. в статьях [Регистрация поставщика](registering-a-provider.md) и [Получение события WMI](receiving-a-wmi-event.md).

 

 



