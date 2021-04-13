---
description: При запуске скрипта в локальной системе, получающей данные из удаленной системы, Инструментарий WMI предоставляет учетные данные поставщику данных в удаленной системе.
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: Делегирование с помощью WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8a624f3d437d977ff73b3854a59cfd634350e7
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424134"
---
# <a name="delegating-with-wmi"></a>Делегирование с помощью WMI

При запуске скрипта в локальной системе, получающей данные из удаленной системы, Инструментарий WMI предоставляет учетные данные поставщику данных в удаленной системе. Для этого требуется только уровень олицетворения **олицетворения**, поскольку требуется только один прыжок сети. Однако если сценарий подключается к WMI в удаленной системе и пытается открыть файл журнала в дополнительной удаленной системе, сценарий завершается ошибкой, если только уровень олицетворения не является **делегатом**. Уровень олицетворения **делегата** требуется для любой операции, включающей более одного прыжка в сеть. Дополнительные сведения о безопасности DCOM в WMI см. в разделе [Установка параметров безопасности процессов для клиентских приложений](setting-client-application-process-security.md). Дополнительные сведения о соединении между двумя компьютерами в односетевой трансляции см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).

**Использование делегирования для подключения к компьютеру через другой компьютер**

1.  Включите делегирование в Active Directory (**Active Directory пользователи и компьютеры** в **административных задачах** **панели управления** ) на контроллере домена. Учетная запись в удаленной системе должна быть помечена как **Доверенная для делегирования** , а учетная запись в локальной системе не должна быть помечена как **учетная запись конфиденциальная и не может быть делегирована**. Локальная система, удаленная система и контроллер домена должны быть членами одного домена или доверенных доменов.

    **Примечание**  .  Использование делегирования является угрозой безопасности, так как предоставляет процессам за пределами прямого управления возможность использования ваших учетных данных.

2.  Измените код следующим образом, чтобы указать, что вы хотите использовать делегирование.

    <dl> <dt>

    <span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>Оболочк
    </dt> <dd>

    Задайте параметр *-Impersonation* в командлете WMI для **делегирования**.

    </dd> <dt>

    <span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>Сценариев
    </dt> <dd>

    Задайте для параметра *имперсонатионлевел* значение **Delegate** в вызове [SWbemLocator. коннектсервер](swbemlocator-connectserver.md) или **Delegate** в строке [моникера](constructing-a-moniker-string.md) . Олицетворение также можно задать в объекте [**свбемсекурити**](swbemsecurity.md).

    </dd> <dt>

    <span id="C__"></span><span id="c__"></span>C++
    </dt> <dd>

    Задайте для параметра уровня олицетворения **\_ \_ \_ \_ делегат уровня "RPC C** " в вызове [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) или [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Дополнительные сведения о том, когда следует выполнять эти вызовы, см. [в разделе Инициализация COM для приложения WMI](initializing-com-for-a-wmi-application.md).

    Чтобы передать удостоверение клиента удаленным COM-серверам в C++, установите маскировку в вызове [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Дополнительные сведения см. в разделе [маскировка](../com/cloaking.md).

    </dd> </dl>

## <a name="examples"></a>Примеры

В следующем примере кода показана строка моникера, которая задает **Делегирование** олицетворения. Имейте в виду, что для центра необходимо задать значение Kerberos.


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



В следующем примере кода показано, как настроить олицетворение для **делегирования** (значение 4) с помощью [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md).


```vb
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = objLocator.ConnectServer(Computer_B, _
                                             "Root\CIMv2", _
                                             AdminAccount, _
                                             MyPassword, _
                                             "kerberos:Domain\Computer_B")
objWMIService.Security_.ImpersonationLevel = 4
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Защита удаленного WMI-подключения](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Удаленное создание процессов с помощью WMI](creating-processes-remotely.md)
</dt> </dl>

 

 
