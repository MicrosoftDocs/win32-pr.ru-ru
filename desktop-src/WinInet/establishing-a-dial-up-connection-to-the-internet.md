---
title: Установка коммутируемого подключения к Интернету
description: Для управления подключениями через модем используются следующие функции.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ac81096d657453d1ebaa0182f39d31af0fe96c01e73122a2de6e0ba9a765e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955594"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a>Установка коммутируемого подключения к Интернету

Для управления подключениями через модем используются следующие функции.

-   [**интернетаутодиал**](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [**интернетаутодиалхангуп**](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [**интернетдиал**](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [**интернетжетконнектедстате**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [**интернетжетконнектедстатикс**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [**интернесангуп**](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [**интернетгунлине**](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> Функции WinINet-подключения не поддерживают двойное соединение, проверку подлинности смарт-карты или соединения, требующие сертификации на основе реестра.

 

> [!Note]  
> начиная с Windows Vista и Windows Server 2008, функции удаленного доступа WinINet используют [функции RAS](/windows/desktop/RRAS/remote-access-service-functions) для установления коммутируемого подключения. WinINet поддерживает функциональные возможности, описанные в функции [**расдиалдлг**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) .

 

> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. для серверных реализаций или служб используйте [Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 