---
description: Windows 8, Windows Server 2012 и более поздние версии включают новую функцию диспетчера подключений, которая позволяет пользователям легко подключаться к Интернету и другим сетям (например, к рабочим и домашним сетям).
ms.assetid: 6b2f5a50-fabd-4c80-acc8-a0883c939632
title: Интерфейсы API беспроводного пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5814ea8daa55ab3ec1bf431543174cf57fdfa7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547087"
---
# <a name="wireless-user-interface-apis"></a>Интерфейсы API беспроводного пользовательского интерфейса

Windows 8, Windows Server 2012 и более поздние версии включают новую функцию диспетчера подключений, которая позволяет пользователям легко подключаться к Интернету и другим сетям (например, к рабочим и домашним сетям). Эта новая функция диспетчера соединений заменяет старое **Подключение к сети** и управление пользовательскими интерфейсами **беспроводных сетей** , включенными в более старые версии Windows для управления собственными подключениями WiFi.

В Windows 7, Windows Server 2008 и Windows Vista существует ряд пользовательских интерфейсов (UI), используемых для подключения или настройки беспроводной сети. Эти пользовательские интерфейсы могут запускаться в приложении с помощью собственных функций Wi-Fi и оболочки Windows. Эти интерфейсы недоступны в Windows 8, Windows Server 2012 и более поздних версиях.

**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Вы не можете запустить какой-либо пользовательский интерфейс, используемый для подключения или настройки беспроводной сети в приложении программным способом.

## <a name="connect-to-a-network"></a>Подключение к сети

В Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 и Windows Vista для установления подключения к беспроводной сети можно использовать мастер **подключения к сети** . Для запуска мастера **подключения к сети** можно использовать функцию [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) .

В следующем коде показан вызов [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) , который запускает мастер **подключения к сети** .


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <shellapi.h>

// Need to link with shell32.lib
#pragma comment(lib, "shell32.lib")

void wmain()
{
   ShellExecute(
      NULL, 
      L"open", 
      L"shell:::{21EC2020-3AEA-1069-A2DD-08002B30309D}\\::{38a98528-6cbf-4ca9-8dc0-b1e1d10f7b1b}",
      NULL,
      NULL,
      SW_SHOWNORMAL);
}
```



## <a name="manage-wireless-networks"></a>**Управление беспроводными сетями**

В Windows 7, Windows Server 2008 и Windows Vista элемент панели управления **Беспроводные** сети используется для управления профилями беспроводной сети. Функцию [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) можно также использовать для запуска элемента **Управление беспроводными сетями** . При вызове **ShellExecute** в Windows 7 и Windows Vista используется следующий путь:

`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.

В следующем примере кода показано, как использовать [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) для запуска мастера **управляемых беспроводных сетей** из приложения.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <shellapi.h>
#include <stdio.h>

// Need to link with shell32.lib
#pragma comment(lib, "shell32.lib")

int wmain()
{

    //-----------------------------------------
    // Declare and initialize variables
    HINSTANCE nResult;

    PCWSTR lpOperation = L"open";    
    PCWSTR lpFile= 
        L"shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\\3\\::{1fa9085f-25a2-489b-85d4-86326eedcd87}";

    nResult = ShellExecute(
        NULL,   // Hwnd
        lpOperation, // do not request elevation unless needed
        lpFile,
        NULL, // no parameters 
        NULL, // use current working directory 
        SW_SHOWNORMAL);

    if((int)nResult == SE_ERR_ACCESSDENIED)
    {
        wprintf(L"ShellExecute returned access denied\n");
        wprintf(L"  Executing the ShellExecute command elevated\n"); 

        nResult = ShellExecute(
            NULL,
            L"runas", // Trick for requesting elevation
            lpFile,
            NULL, // no parameters 
            NULL, // use current working directory 
            SW_HIDE);
    }

    if ( (int) nResult < 32) {
        wprintf(L" ShellExecute failed with error %d\n", (int) nResult);
        return 1;
    }    
    else {    
        wprintf(L" ShellExecute succeeded and returned value %d\n", (int) nResult);
        return 0;
    }
}

```



## <a name="advanced-settings-for-wireless-network-profiles"></a>Дополнительные параметры для профилей беспроводной сети

В состав Windows Vista и более поздних версий входит расширенный пользовательский интерфейс, используемый для просмотра и изменения дополнительных параметров профиля беспроводной сети. Вы можете запустить этот расширенный пользовательский интерфейс, вызвав функцию [**влануиедитпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование собственного WiFi](using-native-wifi.md)
</dt> <dt>

[Образцы профиля беспроводной связи](wireless-profile-samples.md)
</dt> <dt>

[**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[**влануиедитпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 
