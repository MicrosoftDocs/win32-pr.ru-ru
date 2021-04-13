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
# <a name="wireless-user-interface-apis"></a><span data-ttu-id="2dfbd-103">Интерфейсы API беспроводного пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2dfbd-103">Wireless User Interface APIs</span></span>

<span data-ttu-id="2dfbd-104">Windows 8, Windows Server 2012 и более поздние версии включают новую функцию диспетчера подключений, которая позволяет пользователям легко подключаться к Интернету и другим сетям (например, к рабочим и домашним сетям).</span><span class="sxs-lookup"><span data-stu-id="2dfbd-104">Windows 8, Windows Server 2012, and later include a new Connection Manager feature that allows users to easily connect to the Internet and to other networks (work and home networks, for example).</span></span> <span data-ttu-id="2dfbd-105">Эта новая функция диспетчера соединений заменяет старое **Подключение к сети** и управление пользовательскими интерфейсами **беспроводных сетей** , включенными в более старые версии Windows для управления собственными подключениями WiFi.</span><span class="sxs-lookup"><span data-stu-id="2dfbd-105">This new Connection Manager feature replaces the older **Connect to a network** and **Manage Wireless Networks** user interfaces included with older versions of Windows for managing Native Wifi connections.</span></span>

<span data-ttu-id="2dfbd-106">В Windows 7, Windows Server 2008 и Windows Vista существует ряд пользовательских интерфейсов (UI), используемых для подключения или настройки беспроводной сети.</span><span class="sxs-lookup"><span data-stu-id="2dfbd-106">On Windows 7, Windows Server 2008, and Windows Vista, there are a number of user interfaces (UIs) used to connect to or configure a wireless network.</span></span> <span data-ttu-id="2dfbd-107">Эти пользовательские интерфейсы могут запускаться в приложении с помощью собственных функций Wi-Fi и оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="2dfbd-107">These UIs can be started in an application using Native Wifi and Windows Shell functions.</span></span> <span data-ttu-id="2dfbd-108">Эти интерфейсы недоступны в Windows 8, Windows Server 2012 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="2dfbd-108">These UIs are not available on Windows 8, Windows Server 2012, and later.</span></span>

<span data-ttu-id="2dfbd-109">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Вы не можете запустить какой-либо пользовательский интерфейс, используемый для подключения или настройки беспроводной сети в приложении программным способом.</span><span class="sxs-lookup"><span data-stu-id="2dfbd-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** You cannot start any UI used to connect to or configure a wireless network in an application programmatically.</span></span>

## <a name="connect-to-a-network"></a><span data-ttu-id="2dfbd-110">Подключение к сети</span><span class="sxs-lookup"><span data-stu-id="2dfbd-110">Connect to a network</span></span>

<span data-ttu-id="2dfbd-111">В Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 и Windows Vista для установления подключения к беспроводной сети можно использовать мастер **подключения к сети** .</span><span class="sxs-lookup"><span data-stu-id="2dfbd-111">On Windows 8, Windows Server 2012, Windows 7, Windows Server 2008, and Windows Vista, the **Connect to a network** wizard can be used to establish a connection to a wireless network.</span></span> <span data-ttu-id="2dfbd-112">Для запуска мастера **подключения к сети** можно использовать функцию [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="2dfbd-112">You can use the [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function to start the **Connect to a network** wizard.</span></span>

<span data-ttu-id="2dfbd-113">В следующем коде показан вызов [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) , который запускает мастер **подключения к сети** .</span><span class="sxs-lookup"><span data-stu-id="2dfbd-113">The following code shows a [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) call that starts the **Connect to a network** wizard.</span></span>


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



## <a name="manage-wireless-networks"></a><span data-ttu-id="2dfbd-114">**Управление беспроводными сетями**</span><span class="sxs-lookup"><span data-stu-id="2dfbd-114">**Manage Wireless Networks**</span></span>

<span data-ttu-id="2dfbd-115">В Windows 7, Windows Server 2008 и Windows Vista элемент панели управления **Беспроводные** сети используется для управления профилями беспроводной сети.</span><span class="sxs-lookup"><span data-stu-id="2dfbd-115">On Windows 7, Windows Server 2008, and Windows Vista, the **Manage Wireless Networks** Control Panel item is used to manage wireless network profiles.</span></span> <span data-ttu-id="2dfbd-116">Функцию [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) можно также использовать для запуска элемента **Управление беспроводными сетями** .</span><span class="sxs-lookup"><span data-stu-id="2dfbd-116">The [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function can also be used to start the **Manage Wireless Networks** item.</span></span> <span data-ttu-id="2dfbd-117">При вызове **ShellExecute** в Windows 7 и Windows Vista используется следующий путь:</span><span class="sxs-lookup"><span data-stu-id="2dfbd-117">The path to use when calling **ShellExecute** on Windows 7 and Windows Vista is the following:</span></span>

<span data-ttu-id="2dfbd-118">`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.</span><span class="sxs-lookup"><span data-stu-id="2dfbd-118">`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.</span></span>

<span data-ttu-id="2dfbd-119">В следующем примере кода показано, как использовать [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) для запуска мастера **управляемых беспроводных сетей** из приложения.</span><span class="sxs-lookup"><span data-stu-id="2dfbd-119">The following sample code shows how to use [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) to start the **Managed Wireless Networks** wizard from an application.</span></span>


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



## <a name="advanced-settings-for-wireless-network-profiles"></a><span data-ttu-id="2dfbd-120">Дополнительные параметры для профилей беспроводной сети</span><span class="sxs-lookup"><span data-stu-id="2dfbd-120">Advanced Settings for Wireless Network Profiles</span></span>

<span data-ttu-id="2dfbd-121">В состав Windows Vista и более поздних версий входит расширенный пользовательский интерфейс, используемый для просмотра и изменения дополнительных параметров профиля беспроводной сети.</span><span class="sxs-lookup"><span data-stu-id="2dfbd-121">Windows Vista and later include an advanced user interface that is used to view and edit advanced settings of a wireless network profile.</span></span> <span data-ttu-id="2dfbd-122">Вы можете запустить этот расширенный пользовательский интерфейс, вызвав функцию [**влануиедитпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) .</span><span class="sxs-lookup"><span data-stu-id="2dfbd-122">You can start this advanced UI by calling the [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2dfbd-123">См. также</span><span class="sxs-lookup"><span data-stu-id="2dfbd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dfbd-124">Использование собственного WiFi</span><span class="sxs-lookup"><span data-stu-id="2dfbd-124">Using Native Wifi</span></span>](using-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="2dfbd-125">Образцы профиля беспроводной связи</span><span class="sxs-lookup"><span data-stu-id="2dfbd-125">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

[<span data-ttu-id="2dfbd-126">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="2dfbd-126">**ShellExecute**</span></span>](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[<span data-ttu-id="2dfbd-127">**влануиедитпрофиле**</span><span class="sxs-lookup"><span data-stu-id="2dfbd-127">**WlanUIEditProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 
