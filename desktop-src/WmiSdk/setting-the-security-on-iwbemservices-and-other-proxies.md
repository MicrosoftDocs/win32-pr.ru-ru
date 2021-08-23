---
description: 'В C++ можно настроить безопасность всего процесса, вызвав CoInitializeSecurity перед подключением к WMI через Ивбемлокатор:: Коннектсервер.'
ms.assetid: 83c04a96-3829-4c07-91a7-06e5b75b2c12
ms.tgt_platform: multiple
title: Настройка безопасности для IWbemServices и других прокси-серверов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da997b9d4a8f91cf31e8619af983209d4a07a571932c85304d372379d7f752b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050272"
---
# <a name="setting-the-security-on-iwbemservices-and-other-proxies"></a>Настройка безопасности для IWbemServices и других прокси-серверов

В C++ можно настроить безопасность всего процесса, вызвав [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) перед подключением к WMI через [**Ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Можно также изменить уровень проверки подлинности, уровень олицетворения или службу проверки подлинности в вызове, который получает указатель на прокси-сервер WMI, например [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) или [**ивбемкаллресулт**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult). Вызов [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) также позволяет изменить службу проверки подлинности (Kerberos, NTLM или Negotiate).

скрипты и Visual Basic приложения задают безопасность только для прокси-серверов косвенным образом посредством вызовов [**SWbemServices**](swbemservices.md) и других объектов автоматизации. Дополнительные сведения о настройке и изменении проверки подлинности и олицетворения в скрипте см. в разделе [Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).

Изменение уровней безопасности или служб в основном является проблемой при подключении к инструментарию WMI на удаленном компьютере, работающем под управлением другой операционной системы. Дополнительные сведения см. в разделе [подключение между разными операционными системами](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).

Клиентское приложение подключается к прокси-серверу WMI, используя удостоверение. Удостоверение — это объект данных, состоящий из параметров имени пользователя, пароля и центра. Для клиентского приложения WMI вызов интерфейса [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) создает начальное удостоверение. Метод [**коннектсервер**](swbemlocator-connectserver.md) принимает удостоверение в наборе из трех параметров, которые можно установить в **null** для указания текущего пользователя. Можно также указать параметр, отличный от **null** , для указания конкретного пользователя и домена. если вызов выполнен успешно, **коннектсервер** возвращает указатель, с помощью которого можно получить доступ к различным удаленным процессам, таким как служба WMI или операционная система Windows напрямую.

Как и многие интерфейсы COM, [**коннектсервер**](swbemlocator-connectserver.md) возвращает указатель на прокси-сервер. Прокси — это объект данных, представляющий удаленный процесс, например WMI или удаленный поставщик. COM использует прокси-сервер, чтобы предоставить разработчикам доступ к удаленным данным, как если бы данные были локальными.

Следующие интерфейсы WMI используют прокси-серверы:

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) (объект скрипта [**SwbemServices**](swbemservices.md) )
-   [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**ивбемкаллресулт**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**Ивбемрефрешер**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) (объект скрипта [**свбемрефрешер**](swbemrefresher.md) )

    Обновитель WMI является особым случаем, поскольку ему передается указатель [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , параметры безопасности которого должны быть установлены правильно. Дополнительные сведения об использовании объектов обновления см. [в разделе доступ к данным производительности в C++](accessing-performance-data-in-c--.md).

После получения указателя на удаленный процесс можно выполнить одно из двух действий. Если вы понимаете, что делает процесс, вы можете задать безопасность для указателя и получить доступ к процессу в обычном режиме. В этом случае большинство указателей на службу WMI. Дополнительные сведения см. в разделе [Установка уровней безопасности для WMI-соединения](setting-the-security-levels-on-a-wmi-connection.md). Кроме того, необходимо получить доступ к другому COM-интерфейсу на прокси, например [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release), посредством вызова интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) на прокси-сервере.

## <a name="defaults-and-recommendations"></a>значения по умолчанию и Рекомендации

Распределенная версия модели объектов Component (DCOM) согласовывает службу проверки подлинности по умолчанию (Kerberos, NTLM или Negotiate), и вы не можете указать службу проверки подлинности по умолчанию с помощью [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Указание параметра **RPC \_ C \_ AUTHN \_ Default** в параметре службы проверки подлинности [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) позволяет DCOM выбрать соответствующую службу. Для удаленных подключений служба по умолчанию — Negotiate, которая является рекомендуемой службой для приложений, работающих в доменах Kerberos и не-Kerberos. Для локальных соединений используется стандартная служба проверки подлинности NT LAN Manager (NTLM).

В следующем примере кода показана используемая служба проверки подлинности по умолчанию.


```C++
// The pWbemServices variable is of type IWbemServices*

HRESULT hr = CoSetProxyBlanket(
     pWbemServices,                //Proxy
     RPC_C_AUTHN_DEFAULT,          //Authentication service 
     RPC_C_AUTHZ_DEFAULT,          //Authorization service 
     COLE_DEFAULT_PRINCIPAL,       //Server principal name used 
                                       // by authentication service
     RPC_C_AUTHN_LEVEL_DEFAULT,    //Authentication level
     RPC_C_IMP_LEVEL_IMPERSONATE,  //Impersonation level
     COLE_DEFAULT_AUTHINFO,       //Client identity
     EOAC_DEFAULT                  //Capability flags
     );
```



Пример кода в этом разделе требует наличия следующих инструкций Reference и \# include.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



Для сценариев рекомендуется использовать значения по умолчанию, которые DCOM выбирает для удаленных вызовов. На локальном компьютере нельзя указать службу проверки подлинности для вызовов WMI. Дополнительные сведения см. в разделе [Настройка службы проверки подлинности с помощью VBScript](setting-the-authentication-service-using-vbscript.md) и [Создание строки моникера](constructing-a-moniker-string.md).

 

 
