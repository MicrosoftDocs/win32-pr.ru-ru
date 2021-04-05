---
title: URI ресурсов
description: URI ресурса — это идентификатор для отдельного типа операции управления или значение, используемое службами управления, которые реализуют протокол WS-Management.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 665c73caf5cf636ab7f0a0162f488ff073917984
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533197"
---
# <a name="resource-uris"></a>URI ресурсов

[*URI ресурса*](windows-remote-management-glossary.md) — это идентификатор для отдельного типа операции управления или значение, используемое службами управления, которые реализуют протокол WS-Management. Значением управления может быть температура внутри компьютера. Примером операции управления является запуск остановленной службы или задание квоты пользователя на дисковый том.

## <a name="resource-uri-format"></a>Формат URI ресурса

URI состоит из префикса и пути к ресурсу, как показано в следующем примере:

"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"

Эта спецификация схемы указывает на то, что универсальный код ресурса (URI) основан на версии 1 официального протокола WS-Management и что ресурс является [**консолью Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) в \\ пространстве имен root cimv2 репозитория WMI. Префиксы URI содержат спецификацию схемы, например "schemas.microsoft.com/wbem/wsman/1/wmi", и конкретный тип ресурса, например **Win32 \_ LogicalDisk**. Дополнительные сведения об идентификации конкретного экземпляра класса WMI см. в разделе [Служба удаленного управления Windows и инструментарий WMI](windows-remote-management-and-wmi.md).

Дополнительные сведения см. в разделе [префиксы URI](uri-prefixes.md).

## <a name="types-of-resource-uris"></a>Типы URI ресурсов

Хотя [*инструментарий управления Windows (WMI) (WMI)*](windows-remote-management-glossary.md) является основным источником данных управления для операционных систем на основе Windows, также существуют и другие источники схемы управления.

В следующем списке описываются несколько типов URI ресурсов, используемых служба удаленного управления Windows.

-   URI WMI

    Эта группа URI представляет собой [*модель CIM*](/windows/desktop/WmiSdk/gloss-c) путь к классу, включающий пространство имен и класс.

    URI WMI можно использовать в:

    -   Методы [**сеанса**](session.md)
    -   Методы [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
    -   Методы [**WSMan. креатересаурцелокатор**](wsman-createresourcelocator.md) или [**ивсман. креатересаурцелокатор**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)
    -   Методы [**ResourceLocator**](resourcelocator.md) или [**ивсманресаурцелокатор**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

-   URI IPMI

    Эта группа URI представляет стандартные универсальные коды ресурса (URI) на основе CIM версии 2,9. URI IPMI можно использовать в методах сеанса [**Get**](session-get.md), [**WHERE**](session-put.md), [**Enumerate**](session-enumerate.md) и [](session.md) [**Invoke**](session-invoke.md).

    Например, https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd. Этот ресурс определяется в соответствии со схемой CIM [DMTF.org](https://www.dmtf.org/home) .

-   URI конфигурации WinRM

    Эта группа URI — это операции настройки для конфигурации [*прослушивателя*](windows-remote-management-glossary.md) WinRM.

    https://schemas.microsoft.com/wbem/wsman/1/config/listener может использоваться в методах [**сеанса**](session.md) [**Get**](session-get.md), [**помещает**](session-put.md), [**создает**](session-create.md), [**удаляет**](session-delete.md)и [**перечисляет**](session-enumerate.md).

-   URI [*журнала системных событий*](windows-remote-management-glossary.md) (SEL)

    Эта группа URI подписывается на события сборщика событий из BMC. Вы можете подписываться на эти события с помощью программы командной строки **wevtutil** . Для получения дополнительной информации см. https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.

## <a name="case-sensitivity"></a>Чувствительность к регистру

[*Подключаемый модуль WMI*](windows-remote-management-glossary.md) сохраняет регистр URI ресурса, полученного в запросе. Однако для обеспечения взаимодействия с другими реализациями протокола WS-Management используйте правильный регистр для запрошенного ресурса в URI ресурса. Правильный вариант — это проверка орфографии, определяемая поставщиком ресурсов.

В то время как для URI ресурсов не требуется учитывать регистр, [*фрагмент*](windows-remote-management-glossary.md) кода XML делает это. Фрагмент указывает только одно свойство, а не весь набор свойств ресурса. В случае ресурсов WMI синтаксис фрагмента получает одно свойство из экземпляра ресурса. Например, для получения только свойства **Version** из [**Win32 от \_ операционной**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) системы необходимо использовать фрагмент. Дополнительные сведения о фрагментах см. в разделе "Добавление селектора в объект ResourceLocator или Ивсманресаурцелокатор" в [Служба удаленного управления Windows и WMI](windows-remote-management-and-wmi.md).

В соответствии со [](windows-remote-management-glossary.md) стандартами XML и XPath [*подключаемый модуль WMI*](windows-remote-management-glossary.md) применяет чувствительность к регистру для фрагментов и XML, определяющих входные параметры для метода. Для поддержки стандарта XPath 1.0/Level 1 требуется учитывать регистр. Чтобы получить данные WMI с помощью WinRM, учет регистра означает, что имена классов, свойств и методов WMI должны соответствовать регистру имен, найденных в репозитории WMI.

Дополнительные сведения см. в разделе [Синтаксис XPath](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).

## <a name="case-sensitivity-examples"></a>Примеры чувствительности к регистру

Например, скрипт, получающий свойство **\_ дескриптора безопасности** из экземпляра класса [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) инструментария WMI, не может использовать для имен в пути фрагмента верхний регистр, а только URI. [*Подключаемый модуль WinRM WMI*](windows-remote-management-glossary.md) возвращает ошибку для следующего примера VBScript, поскольку XML-код XPath, указанный для **фрагментпас** , не использует правильный регистр. В репозитории WMI класс написан как " \_ служба Win32".


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



В следующей версии того же примера показано правильное использование варианта для класса [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) и свойства **\_ дескриптора безопасности** .


```VB
ResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_Service/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[О служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dt>

[Удаленное управление оборудованием](remote-hardware-management.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 