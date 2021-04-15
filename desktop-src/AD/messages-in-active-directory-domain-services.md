---
title: Сообщения в домен Active Directory Services
description: Сообщения в домен Active Directory Services работают в Windows 2000 и Windows NT 4,0 с пакетом обновления 6a (SP6a) и более поздней версии с помощью DSClient.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Active Directory сообщений AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6895aee711af04778318cf42920d0b0416725205
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654175"
---
# <a name="messages-in-active-directory-domain-services"></a>Сообщения в домен Active Directory Services

Сообщения в домен Active Directory Services работают в Windows 2000 и Windows NT 4,0 с пакетом обновления 6a (SP6a) и более поздней версии с помощью DSClient. Они также работают на рабочих станциях Windows 98/95 с IE 4.01 и более поздних версий и DSClient. Однако если в оболочке запускаются страницы свойств из многовариантного выбора, то сообщение [**\_ \_ \_ об ошибке WM адспроп notify**](wm-adsprop-notify-error.md) и соответствующие вспомогательные функции, [**адспропсендеррормессаже**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) и [**адспропшоверрордиалог**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) не работают и не будут отображаться. Если в средстве администрирования запущены страницы свойств, например пользователи и компьютеры AD, то все сообщения будут работать и доступны для отображения на страницах свойств с выборкой.

Службы домен Active Directory Services используют следующие сообщения:

-   [**\_ \_ применение уведомления WM \_ адспроп**](wm-adsprop-notify-apply.md)
-   [**\_ \_ изменение уведомления WM \_ адспроп**](wm-adsprop-notify-change.md)
-   [**\_ \_ ошибка уведомления адспроп \_ WM**](wm-adsprop-notify-error.md)
-   [**\_ \_ выход из уведомления WM адспроп \_**](wm-adsprop-notify-exit.md)
-   [**\_ \_ \_ передний план уведомления WM адспроп**](wm-adsprop-notify-foreground.md)
-   [**WM \_ адспроп \_ Notify \_ пажехвнд**](wm-adsprop-notify-pagehwnd.md)
-   [**WM \_ адспроп \_ Notify \_ пажеинит**](wm-adsprop-notify-pageinit.md)
-   [**WM \_ адспроп \_ уведомлять \_ SETFOCUS**](wm-adsprop-notify-setfocus.md)
-   [**\_ \_ Создание листа WM \_ адспроп**](wm-adsprop-sheet-create.md)
-   [**\_ \_ \_ уведомление о закрытии листа WM DSA \_**](wm-dsa-sheet-close-notify.md)
-   [**\_ \_ \_ уведомление о создании листа WM DSA \_**](wm-dsa-sheet-create-notify.md)

 

 




