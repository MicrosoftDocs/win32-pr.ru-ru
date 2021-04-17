---
title: служба удаленного управления Windows и WMI
description: Служба удаленного управления Windows можно использовать для получения данных, предоставляемых инструментарий управления Windows (WMI).
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6942e89ea2e63ef809f3452e6ce55a493662c938
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105693938"
---
# <a name="windows-remote-management-and-wmi"></a>служба удаленного управления Windows и WMI

Служба удаленного управления Windows можно использовать для получения данных, предоставляемых инструментарий управления Windows (WMI) ([WMI](/windows/desktop/WmiSdk/wmi-start-page) и [MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)). Данные WMI можно получить с помощью скриптов или приложений, использующих [API-интерфейсы WinRM](winrm-scripting-api.md) или с помощью программы командной строки **WinRM** .

WinRM поддерживает большинство знакомых классов и операций WMI, включая внедренные объекты. WinRM может использовать инструментарий WMI для получения данных о [*ресурсах*](windows-remote-management-glossary.md) или управлении ресурсами в операционной системе на основе Windows. Это означает, что вы можете получать данные об объектах, таких как диски, сетевые адаптеры, службы или процессы в Организации, с помощью существующего набора [классов WMI](/windows/desktop/WmiSdk/wmi-classes). Вы также можете получить доступ к данным оборудования, доступным в стандартном [поставщике IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI.

## <a name="identifying-a-wmi-resource"></a>Определение ресурса WMI

Вы можете ссылаться на класс WMI в качестве [*ресурса*](windows-remote-management-glossary.md) в WinRM и в протоколе WS-Management: тип управляемого объекта, например службы или диска.

Класс или метод WMI идентифицируется по [*универсальному коду ресурса (URI*](windows-remote-management-glossary.md)), как и любой другой ресурс при использовании протокола WS-Management. Универсальный код ресурса (URI) может указывать ресурс WMI (класс), действие WMI (метод) или определять конкретный экземпляр класса в [*сообщениях*](windows-remote-management-glossary.md) , отправляемых по сети. Дополнительные сведения см. в разделе [URI ресурсов](resource-uris.md).

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a>Создание префикса URI для классов WMI

Префикс URI содержит фиксированную часть и пространство имен WMI. Например, префикс URI в Windows Server, содержащий фиксированную часть префикса, — это: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` . Это позволяет создать префикс URI для любого пространства имен WMI. Например, чтобы получить доступ к корневому пространству имен WMI **\\ по умолчанию** , используйте следующий префикс URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .

Большинство классов WMI для управления находятся в корневом пространстве имен **\\ CIMV2** . Чтобы получить доступ к классам и экземплярам в **корневом пространстве имен \\ CIMV2** , используйте префикс URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` . Дополнительные сведения см. в разделе [URI ресурсов](resource-uris.md).

## <a name="generating-a-complete-uri-for-wmi-classes"></a>Создание полного URI для классов WMI

Предоставленный универсальный код ресурса (URI) для программы командной строки **WinRM** или скрипта состоит из префикса и спецификации ресурсов.

В следующей процедуре описывается создание URI ресурса для получения класса WMI или для использования в операции перечисления.

**Создание URI ресурса для класса WMI**

1.  Начните с префикса, указывающего на необходимость использования схемы протокола WS-Management.

    https://schemas.microsoft.com/wbem/wsman/1

    Префикс URI ресурса для классов WMI всегда совпадает. Дополнительные сведения см. в разделе [префиксы URI](uri-prefixes.md).

2.  Добавьте пространство имен WMI к префиксу.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  Добавьте имя класса.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  Чтобы задать значение свойства или вызвать конкретный метод, добавьте требуемое значение ключа или значения для класса.

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    Если оставить значение ключа пустым, исходное значение свойства не будет изменено.

    > [!Note]  
    > Если оставить значение ключа пустым, значение свойства будет равно **null**.

     

## <a name="locating-a-wmi-resource-with-winrm"></a>Поиск ресурса WMI с помощью WinRM

Данные WMI можно получить с помощью программы командной строки, **WinRM** или скрипта Visual Basic, использующего [API-интерфейс для сценариев WinRM](winrm-scripting-api.md). Не используйте [путь WMI](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) для поиска ресурса. Вместо этого необходимо преобразовать пространство имен и иерархию WMI в [*универсальный код ресурса (URI)*](windows-remote-management-glossary.md).

URI WinRM для класса WMI содержит две части: [префикс URI](uri-prefixes.md) и класс, к которому требуется получить доступ.

Например, следующий универсальный код ресурса (URI) может быть передано методу [**Session. Enumerate**](session-enumerate.md) для вывода списка всех служб на компьютере. Префикс URI — `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` , а класс — [**\_ служба Win32**](/windows/desktop/CIMWin32Prov/win32-service).

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

В инструментарии WMI перечислите данные для всех экземпляров ресурса или класса несколькими способами.

-   Запрос для всех экземпляров этого ресурса.

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   Вызов [**SwbemServices. инстанцесоф**](/windows/desktop/WmiSdk/swbemservices-instancesof) или [**\_ SWbemObject. Instances**](/windows/desktop/WmiSdk/swbemobject-instances-).

    `Set colServices = InstancesOf("Win32_Service")`

В WinRM существует один способ перечисления всех экземпляров ресурса: [**Session. Enumerate**](session-enumerate.md).


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a>Поиск конкретного экземпляра ресурса WMI

В инструментарии WMI можно назначить определенный экземпляр класса либо путем указания значений для ключевых свойств, либо путем запроса экземпляра, который соответствует списку значений свойств. Ключевые свойства имеют [**квалификатор ключа**](/windows/desktop/WmiSdk/key-qualifier)WMI.

Получить конкретный экземпляр класса можно несколькими способами.

-   Вызов [**Session. Enumerate**](session-enumerate.md) с параметрами *Filter* и *диалект* для создания запроса.

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   Вызов [**SwbemServices. Get**](/windows/desktop/WmiSdk/swbemservices-get). Для [**сеанса. Get**](session-get.md)необходимо указать одно или несколько конкретных ключевых значений, перед которыми стоит вопросительный знак (?).

    Формат URI для конкретного экземпляра — `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    Класс WMI может иметь более одного ключа. Пары "имя-значение" ключа разделяются знаком "+". В этом случае используется формат: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .

    Синтаксис WinRM для получения Singleton-объекта WMI отличается от WMI. Singleton — это класс WMI, определенный таким образом, что допускается только один экземпляр. [**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) или [**Win32 \_ вмисеттинг**](/windows/desktop/CIMWin32Prov/win32-wmisetting) являются примерами одноэлементного класса WMI.

    Синтаксис WMI для Singleton показан в следующем примере кода VBScript.

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    В следующем примере показан одноэлементный синтаксис WinRM, в котором не используется символ "@".

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   Добавление [*селектора*](windows-remote-management-glossary.md) к объекту [**ResourceLocator**](resourcelocator.md) или [**ивсманресаурцелокатор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) .

    В следующем примере кода VBScript показано, как использовать селектор для получения конкретного экземпляра [**\_ процессора Win32**](/windows/desktop/CIMWin32Prov/win32-processor).

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[О служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dt>

[Префиксы URI](uri-prefixes.md)
</dt> <dt>

[URI ресурсов](resource-uris.md)
</dt> <dt>

[Создание сценариев в служба удаленного управления Windows](scripting-in-windows-remote-management.md)
</dt> </dl>
