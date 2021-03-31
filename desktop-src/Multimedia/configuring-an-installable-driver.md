---
title: Настройка устанавливаемого драйвера
description: Настройка устанавливаемого драйвера
ms.assetid: c81f4bcb-38c6-42f1-a50d-1f700c6a3c37
keywords:
- устанавливаемые драйверы, Настройка
- Настройка устанавливаемых драйверов
- Функция Опендривер
- Функция Сенддривермессаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad0ad16d719152dba0dc0b2ca6224122831a0ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069834"
---
# <a name="configuring-an-installable-driver"></a><span data-ttu-id="ffb57-107">Настройка устанавливаемого драйвера</span><span class="sxs-lookup"><span data-stu-id="ffb57-107">Configuring an Installable Driver</span></span>

<span data-ttu-id="ffb57-108">Чтобы направить устанавливаемый драйвер для выполнения полезных задач, необходимо открыть драйвер с помощью функции [опендривер](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) и отправить сообщения с помощью функции [сенддривермессаже](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) .</span><span class="sxs-lookup"><span data-stu-id="ffb57-108">To direct an installable driver to carry out useful tasks, you must open the driver by using the [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) function and send it messages by using the [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) function.</span></span> <span data-ttu-id="ffb57-109">В следующем примере показано, как настроить драйвер для отображения диалогового окна настройки.</span><span class="sxs-lookup"><span data-stu-id="ffb57-109">The following example shows how to direct the driver to display its configuration dialog box.</span></span>


```C++
LONG MyConfigureDriver()
{
    HDRVR hdrvr;
    DRVCONFIGINFO dci;
    LONG lRes;

    // Open the driver (no additional parameters needed this time).
    if ((hdrvr = OpenDriver(L"\\samples\\sample.drv", 0, 0)) == 0) {
        // Can't open the driver
        return DRVCNF_CANCEL;
    }

    // Make sure driver has a configuration dialog box.
    if (SendDriverMessage(hdrvr, DRV_QUERYCONFIGURE, 0, 0) != 0) {
        // Set the DRVCONFIGINFO structure and send the message
        dci.dwDCISize = sizeof (dci);
        dci.lpszDCISectionName = (LPWSTR)0;
        dci.lpszDCIAliasName = (LPWSTR)0;
        lRes = SendDriverMessage(hdrvr, DRV_CONFIGURE, 0, (LONG)&dci);
     }

    // Close the driver (no additional parameters needed this time).
    CloseDriver(hdrvr, 0, 0);

    return lRes;
}
 
```



 

 