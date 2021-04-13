---
description: При выполнении вызовов за пределами вызывающего процесса или удаленной службы WMI WMI использует распределенную версию модели объектов Component (DCOM).
ms.assetid: 261b4f18-5de5-4e06-a887-f5afd9c45511
ms.tgt_platform: multiple
title: Настройка проверки подлинности в WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0293d74c528e7c1c0e77a1ffb9f5f9ee7dfd5f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265369"
---
# <a name="setting-authentication-in-wmi"></a>Настройка проверки подлинности в WMI

При выполнении вызовов за пределами вызывающего процесса или удаленной службы WMI WMI использует распределенную версию модели объектов Component (DCOM). Необработанные и удаленные вызовы выполняются через прокси-серверы, для которых требуется проверка подлинности учетных данных вызывающего процесса.

Уровень проверки подлинности задается при подключении к компьютеру и пространству имен WMI. Чтобы подключиться к инструментарию WMI, вызовите [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) в C++. В сценариях или Visual Basic вы подключаетесь к WMI с помощью SWbemLocator. Коннектсервер или через строку [моникера](constructing-a-moniker-string.md) . При соединении между компьютерами безопасность DCOM и инструментарий WMI должны иметь определенные уровни проверки подлинности. Требуемый уровень зависит от операционной системы, к которой выполняется подключение. Дополнительные сведения см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).

Как правило, WMI работает на узле общей службы и использует ту же проверку подлинности, что и другие процессы в узле. Чтобы запустить WMI-процесс с другим уровнем проверки подлинности, запустите WMI с помощью команды [**Winmgmt**](winmgmt.md) с параметром **/стандалонехост** и установите уровень проверки подлинности для WMI как обычно. Дополнительные сведения см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).

Дополнительные сведения и примеры кода для настройки проверки подлинности для соединений WMI см. в разделе [Настройка службы проверки подлинности с помощью VBScript](setting-the-authentication-service-using-vbscript.md) и [Настройка проверки подлинности с помощью C++](setting-authentication-using-c-.md). В этих разделах также содержатся таблицы, в которых перечислены константы проверки подлинности для C++ и сценариев.

## <a name="using-proxies-in-wmi"></a>Использование прокси-серверов в WMI

Чтобы задать проверку подлинности для прокси-сервера, вызовите функцию [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) . Дополнительные сведения и пример кода см. в разделе [Настройка параметров безопасности для IWbemServices и других учетных записей-посредников](setting-the-security-on-iwbemservices-and-other-proxies.md).

Следующий [API COM для объектов WMI](com-api-for-wmi.md) использует прокси-серверы непосредственно в C++ или C# для вызова из процесса или удаленной службы WMI:

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)
-   [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**ивбемкаллресулт**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**ивбемрефрешер**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)

Объекты скриптов, такие как [**SWbemObject**](swbemobject.md), [**SwbemServices**](swbemservices.md)и [**свбемрефрешер**](swbemrefresher.md) , не используют прокси-серверы напрямую. Вместо этого объекты скрипта представляют оболочку или слой, который вызывает [API COM для объектов WMI](com-api-for-wmi.md) , перечисленных выше. Дополнительные сведения и пример кода для настройки проверки подлинности в скриптах см. в разделе [Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
