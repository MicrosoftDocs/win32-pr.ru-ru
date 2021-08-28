---
description: Перед реализацией поставщика необходимо сначала зарегистрировать поставщик в WMI. Регистрация поставщика определяет тип поставщика и классы, которые поддерживает поставщик. Инструментарий WMI может обращаться только к зарегистрированным поставщикам.
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: Регистрация поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265d3a9f8617c68793fc30c0dc23fd3e9f0106ee98a9e3c757754e2fe589dda8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995924"
---
# <a name="registering-a-provider"></a>Регистрация поставщика

Перед реализацией поставщика необходимо сначала зарегистрировать поставщик в WMI. Регистрация поставщика определяет тип поставщика и классы, которые поддерживает поставщик. Инструментарий WMI может обращаться только к зарегистрированным поставщикам.

> [!Note]  
> Дополнительные сведения о регистрации поставщика MI см. в разделе [практические руководства. Регистрация поставщика MI](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).

 

Вы можете написать свой код поставщика перед регистрацией поставщика. Однако очень сложно отлаживать поставщик, не зарегистрированный в WMI. Определение интерфейсов для поставщика также помогает структурировать назначение и структуру поставщика. Поэтому регистрация поставщика помогает в проектировании поставщика.

Только администраторы могут регистрировать или удалять поставщик.

Поставщик должен быть зарегистрирован для всех различных типов функций поставщика, которые он выполняет. Почти все поставщики предоставляют экземпляры классов, которые они определяют, но они также могут предоставлять данные свойств, методы, события или классы. Поставщик также может быть зарегистрирован в качестве поставщика объекта события или поставщика счетчика производительности. Рекомендуется объединить все функциональные возможности поставщика в одном поставщике, а не иметь много отдельных поставщиков для каждого типа. Примером является [поставщик системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider), предоставляющий методы и экземпляры, а также [поставщик дисковых квот](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), предоставляющий экземпляры, методы и события.

Поставщик должен быть зарегистрирован для всех различных типов функций поставщика, которые он выполняет. Почти все поставщики предоставляют экземпляры классов, которые они определяют, но они также могут предоставлять данные свойств, методы, события или классы. Поставщик также может быть зарегистрирован в качестве поставщика объекта события или поставщика счетчика производительности.

Для каждого типа регистрации используется один и тот же экземпляр [**\_ \_ Win32Provider**](--win32provider.md) :

-   [Регистрация поставщика экземпляра](registering-an-instance-provider.md)
-   [Регистрация поставщика класса](registering-a-class-provider.md)
-   [Регистрация поставщика методов](registering-a-method-provider.md)
-   [Регистрация поставщика событий](registering-an-event-provider.md)
-   [Регистрация поставщика событий-получателя](registering-an-event-consumer-provider.md)
-   [Создание поставщика экземпляров в поставщике High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a>Пример. Создание и регистрация экземпляра поставщика

В следующем примере показан MOF-файл, который создает и регистрирует экземпляр [поставщика системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider) в корневом \\ пространстве имен CIMV2. Он назначает поставщику $Reg псевдонима, чтобы избежать длинного пути, необходимого для регистрации экземпляра и метода. Дополнительные сведения см. в разделе [Создание псевдонима](creating-an-alias.md).

``` syntax
// Place the Registry provider in the root\cimv2 namespace
#pragma namespace("\\\\.\\ROOT\\cimv2")

// Create an instance of __Win32Provider
instance of __Win32Provider as $Reg
{
Name = "RegProv";        
CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
HostingModel = "NetworkServiceHost:LocalServiceHost";
};

// Register as an instance provider by
// creating an instance
// of __InstanceProviderRegistration
instance of __InstanceProviderRegistration
{
 provider = $Reg;
 SupportsDelete = FALSE;
 SupportsEnumeration = TRUE;
 SupportsGet = TRUE;
 SupportsPut = TRUE;
};

// Register as a method provider by
// creating an instance
// of __MethodProviderRegistration
instance of __MethodProviderRegistration
{
 provider = $Reg;
};

// Define the StdRegProv class
[dynamic: ToInstance, provider("RegProv")]
class StdRegProv
{
[implemented, static] uint32 CreateKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 DeleteKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 EnumKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[]);
[implemented, static] uint32 EnumValues(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[], 
 [OUT] sint32 Types[]);
[implemented, static] uint32 DeleteValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName);
 [implemented, static] uint32 SetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] uint32 uValue = 3);
[implemented, static] uint32 GetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint32 uValue);
[implemented, static] uint32 SetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "hello");
[implemented, static] uint32 GetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue[] = {"hello", "there"});
[implemented, static] uint32 GetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue[]);
[implemented, static] uint32 SetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "%path%");
[implemented, static] uint32 GetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetBinaryValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [in] uint8 uValue[] = {1, 2});
[implemented, static] uint32 GetBinaryValue(
 {IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint8 uValue[]);
[implemented, static] uint32 CheckAccess(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] uint32 uRequired = 3, 
 [OUT] boolean bGranted);
};
```

## <a name="example-registering-a-provider"></a>Пример. Регистрация поставщика

В следующей процедуре описывается регистрация поставщика.

**Регистрация поставщика**

1.  Зарегистрируйте поставщик в качестве сервера COM.

    При необходимости может потребоваться создать записи реестра. Этот процесс применяется ко всем COM-серверам и не связан с WMI. дополнительные сведения см. в разделе COM документации по пакету Microsoft Windows Software Development Kit (SDK).

2.  Создайте MOF-файл, содержащий экземпляры [**\_ \_ Win32Provider**](--win32provider.md) и экземпляр класса, производный непосредственно или косвенно от [**\_ \_ провидеррегистратион**](--providerregistration.md), например [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md). Только администраторы могут регистрировать или удалять поставщик, создавая экземпляры классов, производных от **\_ \_ Win32Provider** или [**\_ \_ провидеррегистратион**](--providerregistration.md).
3.  Задайте [**хостингмодел**](--win32provider.md) в экземпляре **\_ \_ Win32Provider** в соответствии со значениями в [моделях размещения](provider-hosting-and-security.md).

    > [!Note]  
    > Если поставщик не требует высокой привилегий учетной записи LocalSystem, свойство [**\_ \_ Win32Provider. хостингмодел**](--win32provider.md) должно иметь значение "нетворксервицехост". Дополнительные сведения см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).

     

    В следующем примере MOF из полного примера показан код, создающий экземпляр [**\_ \_ Win32Provider**](--win32provider.md).

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  Экземпляр класса, производного непосредственно или косвенно от [**\_ \_ провидеррегистратион**](--providerregistration.md), для описания логической реализации поставщика. Поставщик может быть зарегистрирован для нескольких различных типов функциональных возможностей. В приведенном выше примере Регпров регистрируется как экземпляр и поставщик метода. Но если Регпров поддерживает функциональность, ее также можно зарегистрировать в качестве свойства или поставщика событий. В следующей таблице перечислены классы, которые регистрируют функциональность поставщика.

    

    | Классы регистрации поставщика                                                        | Описание                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [**\_\_инстанцепровидеррегистратион**](--instanceproviderregistration.md)           | Регистрирует [поставщик экземпляра](registering-an-instance-provider.md).             |
    | [**\_\_евентпровидеррегистратион**](--eventproviderregistration.md)                 | Регистрирует [поставщик событий](registering-an-event-provider.md).                   |
    | [**\_\_евентконсумерпровидеррегистратион**](--eventconsumerproviderregistration.md) | Регистрирует [поставщик потребителей событий](registering-an-event-consumer-provider.md). |
    | [**\_\_месодпровидеррегистратион**](--methodproviderregistration.md)               | Регистрирует [поставщик метода](registering-an-event-consumer-provider.md).          |
    | [**\_\_пропертипровидеррегистратион**](--propertyproviderregistration.md)           | Регистрирует [поставщик свойств](registering-a-property-provider.md).               |

    

     

5.  Поместите MOF-файл в постоянный каталог.

    Как правило, файл следует поместить в каталог установки поставщика.

6.  Скомпилируйте MOF-файл с помощью [mofcomp](mofcomp.md) или интерфейса [**имофкомпилер**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

    Дополнительные сведения см. в разделе [Компиляция MOF-файлов](compiling-mof-files.md).

    **Windows 8 и Windows Server 2012:** При установке поставщиков и [**mofcomp**](mofcomp.md) , и интерфейс [**имофкомпилер**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) рассматривают \[ ключ \] и \[ статические \] Квалификаторы как true, если они есть, независимо от их реальных значений. Другие квалификаторы обрабатываются как false, если они есть, но не имеют явного значения true.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Разработка поставщика WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Настройка дескрипторов безопасности Намепаце](setting-namespace-security-descriptors.md)
</dt> <dt>

[Защита поставщика](securing-your-provider.md)
</dt> </dl>

 

 
