---
description: Чтобы создать поставщик событий WMI, необходимо зарегистрировать \_ \_ экземпляр Win32Provider, представляющий поставщика, с помощью экземпляра \_ \_ евентпровидеррегистратион.
ms.assetid: 81f2ba3b-a1cb-42f5-b1a7-b1ca65963902
ms.tgt_platform: multiple
title: Регистрация поставщика событий
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a4aa77c5c5936639435844179f259080085e02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156763"
---
# <a name="registering-an-event-provider"></a>Регистрация поставщика событий

Чтобы создать [*поставщик событий*](gloss-e.md) WMI, необходимо зарегистрировать экземпляр [**\_ \_ Win32Provider**](--win32provider.md) , представляющий поставщика, с помощью экземпляра [**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md). В качестве COM-объекта поставщик должен зарегистрироваться в операционной системе и инструментарии WMI. В следующей процедуре предполагается, что вы уже реализовали процесс регистрации, как описано в статье [Регистрация поставщика](registering-a-provider.md).

В следующей процедуре описывается регистрация поставщика событий.

**Регистрация поставщика событий**

1.  Создайте экземпляр класса [**\_ \_ Win32Provider**](--win32provider.md) , который описывает поставщик.
2.  Создайте экземпляр класса [**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md) , описывающий набор функций поставщика.

    Класс [**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md) наследует многие свойства от родительского класса [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md) . Свойства, локальные для класса **\_ \_ евентпровидеррегистратион** , представляют собой путь к объекту поставщика и список запросов, описывающих события, которые поддерживает поставщик. Дополнительные сведения см. в разделе [запрос WMI](querying-wmi.md).

3.  Загрузите реализацию классов [**\_ \_ Win32Provider**](--win32provider.md) и [**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md) в репозиторий WMI.

    Инструментарий WMI использует определение класса для регистрации и доступа к поставщику событий. Дополнительные сведения см. [в разделе Регистрация поставщика](registering-a-provider.md).

В следующем примере кода описывается реализация класса [**\_ \_ Win32Provider**](--win32provider.md) и класса [**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md) .

``` syntax
instance of __Win32Provider as $P
{
    ClientLoadableCLSID = NULL;
    CLSID = "{AA7828C5-95F9-11d2-BB0D-00C042424242}";
    DefaultMachineName = NULL;
    ImpersonationLevel = 0;
    InitializationReentrancy = 0;
    InitializeAsAdminFirst = FALSE;
    Name = "FaxEventProvider";
    PerLocaleInitialization = FALSE;
    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};

instance of __EventProviderRegistration
{  
Provider = $P;
EventQueryList = {
         "SELECT * FROM FaxEvent",
         "SELECT * FROM __InstanceCreationEvent WHERE TargetInstance ISA \"Win32_LogicalDisk\""};
};
```

Первый запрос указывает, что поставщик создает все уведомления о событиях для класса внешних событий Факсевент. Поскольку в нем используется оператор ISA, второй запрос подразумевает, что поставщик создает уведомления для всех событий создания экземпляра для класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) и всех его подклассов.

Когда поставщик регистрируется для предоставления внутреннего события, это событие должно применяться ко всем экземплярам класса. Иными словами, запрос не может быть написан, чтобы предоставить события создания экземпляра только для некоторых дисков, принадлежащих классу [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

 

 
